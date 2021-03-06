Appendix: How TEA Scores Are Calculated
=======================================

This appendix summarizes the operations tranSMART performs to calculate
the overall TEA score for an experiment, and the data inputs that the
calculation requires. Pseudocode representations of the operations being
performed are included where they may clarify the operation.

Data Inputs to the TEA algorithm
--------------------------------

One of the following:

-  A gene signature or gene list containing any number of genes, with a
   binary up- or down-regulation flag based on fold change.

-  A pathway containing any number of genes.

And:

-  A gene search result list for each signature, list, or pathway gene.
   Result lists contain experimental comparisons.

Operations
----------

#. Compute the average fold change and standard deviation for all
   genes in the comparison.

#. Compute a normalized p-value (NPV) for each gene in the
   comparison, based on its fold change (fc) value, and the above
   average (ave) and standard deviation (std) values. Use a normal
   distribution function (CDF)::

       if (fc > 0)

       NPV = 1.0 - CDF(fc, ave, std)

       else

       NPV = 1.0 - CDF(-fc, ave, std)

       if NPV < 1.0e-15, set to 1.0e-15

#. For each gene in the gene signature, list, or pathway, search against
   experimental comparisons and extract those comparisons where the
   gene’s normalized p-value is less than 0.05. This returns a
   comparison list.

#. Iterate through the comparison list. For each comparison (C), add the
   normalized p-value to one of two arrays of sums (`pv_sum`), as
   follows:

   -  For gene signatures and gene lists, add the gene’s normalized p-value to:

   -  ``pv_sum(C, up)`` if the gene’s fold change in the signature (svc)
      *and* in the comparison (cfc) are co-regulated.

   -  ``pv_sum(C, down)`` if the gene’s fold change in the signature *and*
      in the comparison are anti-regulated.

   -  For pathways, add the gene’s normalized p-value to:

   -  ``pv_sum(C, up)`` if the gene’s comparison fold change (cfc) is
      up-regulated.

   -  ``pv_sum(C, down)`` if the gene’s comparison fold change is
      down-regulated.

   Also, use the logarithm of the normalized p-value to make the final TEA score more human readable::

       if (gene_signature OR gene_list)
         if ((sfc > 0 AND cfc > 0) OR (sfc < 0 AND cfc < 0))
           pv_sum(C, up) += -Math.log(NPV)
           pv_count(C, up)++
         else
           pv_sum(C, down) += -Math.log(NPV)
           pv_count(C, down)++

       if (gene_pathway)
         if (cfc > 0)
           pv_sum(C, up) += -Math.log(NPV)
           pv_count(C, up)++
         else
           pv_sum(C, down) += -Math.log(NPV)
           pv_count(C, down)++


#. Compute the min-LogP average (pv_ave) for each sum::

      pv_ave(C, up) = Math.exp(-pv_sum(C,up) / pv_count(C,up))

      pv_ave(C, down) = Math.exp(-pv_sum(C,down) / pv_count(C,down))

#. Compute a TEA score (pv_tea) for each min-LogP average through a
   binomial distribution function::

       pv_tea(C, up) = 1.0 - Binom( N, pv_count(C,up), pv_ave(C,up))

       pv_tea(C, down) = 1.0 - Binom( N, pv_count(C,down), pv_ave(C,down))


Result
------

-  **TEA score**: For gene signatures, lists, and pathways, the final
   TEA score is the more significant pv_tea value (the lower of the two
   pv_tea values).

-  A gene signature or list is determined to be co-regulated or
   anti-regulated as follows:

   -  **Co-regulated**: The more significant pv_tea value was derived
      from the sums associated with co-regulated fold change values
      (pv_sum(C, up)).

   -  **Anti-regulated**: The more significant pv_tea value was derived
      from the sums associated with anti-regulated fold change values
      (pv_sum(C, down)).

-  A pathway is determined to be up-regulated or down-regulated as
   follows:

   -  **Up-regulated**: The more significant pv_tea value was derived
      from the sums associated with up-regulated fold change values
      (pv_sum(C, up)).

   -  **Down-regulated**: The more significant pv_tea value was derived
      from the sums associated with down-regulated fold change values
      (pv_sum(C, down)).
