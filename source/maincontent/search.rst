Search Tool
======================

tranSMART provides a Google-like interface for searching across internal
data sources as well as external data sources with a single query, based
on one or more search filters that you define.

Search Tasks
------------

A search filter is the name of a biomedical concept such as a gene,
pathway, disease, or other item of medical interest. These filter names
are pre-defined in tranSMART. You can browse lists of these filter names
and select the filter you want, or type part of a filter name in the
**Search** field, causing tranSMART to display a list of filters that
begin with the text you type.

You can base your search on a single search filter or on a multi-filter
search string.

Defining a Search Filter
~~~~~~~~~~~~~~~~~~~~~~~~

There are several ways to define a search filter:

-  Type all or part of the filter name directly into the **Search**
   field.

-  Browse all the pre-defined filters within filter categories (such as
   diseases).

-  Use a saved search filter or search string.

Type the Filter Name
^^^^^^^^^^^^^^^^^^^^

To search the internal and external data sources for information related to a filter name:

#. Click the tab for the Search tool at the top of the tranSMART window.

#. Click the search filter category to search within (for example, search only diseases, or search only genes).

  |image7|

  The search engine first filters by the filter category you select, and then filters by the name you type. To search across all filter categories, click **all**:

.. note:: You can only specify one search filter in the **Search** field shown above. For instructions on creating a multi-filter search string, see *Building a Search String*.

#. Type part or all of the filter name into the **Search** field.

  Up to 20 matches that begin with the text you type are displayed in a dropdown list below the **Search** field. For example, the following list appears for the search filter **bra** when searching across all filter categories:

  |image9|

  .. note:: You can also search for aliases. For example, to find the gene PTK7, you can type part or all of the name PTK7 or its alias, CCK4.

#. Do one of the following:

  -  If the name of the filter you want appears in the list, click the
     filter name. The search begins immediately.

  -  If the filter name you want does not appear in the list, type a more
     complete name in the **Search** field. For example, if you typed only
     **br** in the **Search** field, no entries for “brain diseases”
     appear in the list. Typing an **a** after the text you already typed
     displays a list like the one shown above.

  -  If no list appears after you type a complete filter name, click the
     **Search** button.

#. To start another search using a new search filter, click **clear all** above the search result:

   |image11|

Alternatively, you can click the tranSMART logo, or simply type a new
filter in the **Search** field.

See `*Working with Search Results* <#Working_With_Search_Results>`__  for information on viewing and refining search results.

Browse for a Filter Name
^^^^^^^^^^^^^^^^^^^^^^^^

You can browse through all the pre-defined filters in each of the
following areas:

-  Disease

-  Gene Signature/Lists

-  Geo/ebi

-  Pathway

To browse the pre-defined filters:

#. Click the tab for the Search tool at the top of the tranSMART
      window.
#. Click the **browse** link to the right of the **Search** button. A
      window similar to the following appears:

    |image12|

    .. note:: The search engine ignores any filter category you may have    selected and any filter text you may have entered in the **Search** field.

#. Click the tab for the area in which you want to browse for filters.

#. To initiate a search for information related to a filter, click the
   filter name or the green arrow (|image14|) after the name.

   After you click a filter, the search begins immediately.

#. To browse for another filter, click **browse** again. There is no
   need to clear the previous result.

#. To start another search using a new search filter, click **clear
   all** above the search result:

   |image15|

Alternatively, you can click the tranSMART logo, or simply type a new
filter in the **Search** field.

See `*Working with Search Results* <#Working_With_Search_Results>`__ on
page `16 <#Working_With_Search_Results>`__ for information on viewing
and refining search results.

Use a Saved Search Filter
^^^^^^^^^^^^^^^^^^^^^^^^^

There are two ways to access a saved search filter:

-  Retrieve the saved filter from a list of filters that you created and
   saved. The instructions in this section describe this method.

-  Click a link to a saved filter that someone else has created, saved,
   and emailed to you.

See *Saving a Search Filter or Search String* for more information, including instructions on saving search filters and search strings.

To search against a filter that you created and saved:

#. Click the tab for the Search tool at the top of the tranSMART
      window.
#. Click the **saved filters** link to the right of the **Search**
  button. A list of filters that you created and saved appears:

  |image16|

#. To search against a saved filter in the list, click the **select**
   link to the right of the saved filter name. The search begins
   immediately.
#. To start another search using a new search filter, click **clear**
   **all** above the search result.

Alternatively, you can click the tranSMART logo, or simply type a new
filter in the **Search** field.

See *Working with Search Results*  for information on viewing
and refining search results.


Building a Search String
~~~~~~~~~~~~~~~~~~~~~~~~

You can make the scope of your search more precise by building a
multi-filter search string. The filters in a search string are joined by
the logical operators AND and OR.

Rules for Building a Search String
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The following rules apply to building a multi-filter search string:

-  Filters within the same filter category (such as diseases or genes)
   are joined by the logical operator OR.

For example, if you add the filters Diseases> Melanoma and Diseases>
Melanoma, Experimental to a search string, the search engine evaluates
them as in the following expression:

  (Diseases> Melanoma **OR** Diseases> Melanoma, Experimental)

-  Filters within different filter categories are joined by the logical
   operator AND.

For example, if you add the filters Diseases> Anemia, Diseases> Anemia,
Hemolytic, and Gene> HBB to a search string, the search engine evaluates
them as in the following expression:

    (Diseases> Anemia **OR** Diseases> Anemia, Hemolytic) **AND** Gene>
    HBB

-  Filters that are not among the pre-defined filters are assigned to
   the filter category **Text>**.

Instructions for Building a Search String
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. To build a multi-filter search string:
#. Define a search filter using any of the methods described in
      *Defining a Search Filter* .
#. When the results window appears, click **advanced**:

    |image17|

The Edit Filters dialog appears, displaying the filter you just created:

    |image18|
#. To add another filter, type part or all of a filter name into the
   **Search** field.

Up to 20 matches for the text you type are displayed in a dropdown list
below the **Search** field. For example, the following list appears for
the search filter **dis**:

|image19|

Do one of the following:

-  If the name of the filter you want appears in the list, click the
   filter name. The tranSMART software inserts the filter into the
   **Filters Box**.

-  If the filter you want does not appear in the list, type a more
   complete name in the **Search** field.

-  If no list appears after you type a complete filter name, click the
   plus-sign button ( |image20| ) to the right of the **Search** field.
#. Repeat the previous step for each new filter to add to the search
   string.
#. Optionally, to delete a filter from the search string, click the red
   **X** (|image21|) to the right of the filter name:

    |image22|
#. When finished defining the search string, click **Apply** to begin
   the search.
#. When the results window appears, you can continue editing the search
   string or save it, as follows:

-  To continue editing the search string, click **advanced**.

-  To save the search string, click **save**.

   |image23|

The search engine evaluates this search string as in the following
expression:

(Disease> Brain Diseases **OR** Dementia)

See *Saving a Search Filter or Search String*  for more
information about saving search filters and search strings.

Saving a Search Filter or Search String
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. To save a search filter or search string:
#. After defining the search filter or search string, run the search
      and click **save** in the results window.

The Create Filter window appears:

|image24|
#. In the **Name** field, type a name for the search filter or search
   string.
#. Optionally, in the **Description** field, type a description of the
   search filter or search string. In the saved filters list, the
   description appears immediately below the name of the search filter
   or search string.
#. Check the **Private** **Flag** checkbox to prevent others from using
   this search filter or search string, or clear the checkbox to allow
   others to use the search filter or search string.

If a filter is public, a shortcut (link) to the filter is displayed in
the **saved filters** list, and an **email** link is provided, allowing
you to email the shortcut to others. If a filter is private, the saved
filter is marked “Private,” and the filter shortcut and **email** link
are not displayed.

.. note:: Only the person who created and saved a search filter can see that filter in the saved filter list. To let a colleague use a search filter you saved, you must (1) mark the filter as Public, and (2) click the **email** link to send the shortcut for the search filter to the colleague.

In the following **Saved Filters** list, the first two entries are
private and the third is public:

|image26|
#. When finished, click **Create** to save the new search filter or
   search string, or click **Cancel** to abandon it.

Editing and Deleting Saved Filters
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To edit a saved filter:

#. Click the tab for the Search tool at the top of the tranSMART
      window.
#. Click the **saved filters** link to the right of the **Search**
      button. A list of your saved search filters appears.
#. Click the **edit** link to the right of the saved filter name. The
      Edit Filter window appears:

    |image27|
#. Make one or more of the following changes:

-  In the **Name** field, modify the name of the saved filter.

-  In the **Description** field, add or modify an optional description
   of the saved filter. In the **saved filters** list, the description
   appears immediately below the saved filter name.

-  Check the **Private Flag** checkbox to prevent others from using this
   saved filter, or clear the checkbox to allow others to use the saved
   filter.

Another user can use a filter you created and saved only (1) if the
filter is public, and (2) you email the user the shortcut (link) to the
filter.

-  To delete the filter you are editing, click the **Delete** button
   (|image28|).


.. note:: These are the only changes you can make to a saved filter. To make changes to the filter itself, run the search against the filter, then click **advanced** to define a new search filter based on the existing one. For details, see Instructions for *Building a Search String* .

#. When finished making changes, click the **Update** button to save
   your changes, or click the **Cancel** button to abandon them.

#. To delete a saved filter from the saved filters list:
#. Click the tab for the Search tool at the top of the tranSMART
      window.
#. Click the **saved filters** link to the right of the **Search**
      button. A list of saved search filters appears.
#. Click the **delete** link to the right of the saved filter name.

Working with Search Results
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The results window displays all the clinical, documentary, and other
information found in the data warehouse that relates to the search
filter or search string.

The content of the results window varies, depending on the result
category you select (for example, Clinical Trials or mRNA Analysis) and
the type of view you want to use to display the results (for example,
Heatmap or Study View). Some result categories also let you further
refine the results by adding more filters to the search.

To select a result category to view, click the tab that contains the
result category name.

The following figure shows the sections of the results window:

|image30|

The tabs for the result categories Clinical Trials and mRNA Analysis
display pairs of numbers. These numbers represent the following results:

-  **Clinical Trials ( x, y )**

   -  x = the number of statistically significant analyses. These hits
      can be viewed in the Analysis View.

   -  y = the total number of analyses. These hits can be viewed in the
      Study View.

For example, in the preceding figure, 1 statistically significant
analysis was returned, and a total of 45 analyses were returned.

-  **mRNA Analysis (x, y)**

   -  x = the number of statistically significant analyses. These hits
      can be viewed in the Analysis View.

   -  y = the total number of analyses. These hits can be viewed in the
      Study View.

For example, in the preceding figure, 1 statistically significant
analysis was returned, and a total of 3 analyses were returned.

A *statistically significant analysis* is one in which the genes in a
gene signature, gene list, or pathway are differentially modulated in a
statistically significant way, indicating that the associated target or
pathway is probably affected by the treatment, disease or other topic
examined in the study.

To qualify as a statistically significant analysis, certain data points
(such as p-value) must be evaluated and attain an aggregate score that
meets or exceeds a particular threshold, based on an internal algorithm.
For information on the rules that determine how analysis results are
ranked, see *TEA Analyses* .

.. TODO: fix all tyhese page references

The following sections describe the views and operations available for
each result category:

-  *Clinical Trials Tab* (Page 17)

-  *mRNA Analysis Tab* (page 18)

-  *Literature Tab* (page 23)

-  *Documents Tab* (page 23)

Clinical Trials Tab
^^^^^^^^^^^^^^^^^^^

This result category contains data from internal clinical trials.

Click the **Clinical Trials** tab to display the results in this
category. The buttons in the following figure appear at the top of the
results list. You may see fewer buttons, depending on the results of
your particular search:

|image31|

These buttons give you access to the following views and operations:

-  **Show Filters** – Define additional filters to further refine the
   search results.

-  **Heatmap** – View the results as a heat map.

-  **Analysis View** – View a list of the statistically significant
   analyses of the clinical trials.

Results are sorted from the highest-scoring analysis down to the lowest.

-  **Study View** – View a list of the clinical trials and, optionally,
   *all* the analyses for each clinical trial – that is, those analyses
   that are considered statistically significant and those that are not.

Results are sorted from the clinical trial with the most matches with
the search filter or search string, down to the one with the least
matches.

-  **Export Results** – Export descriptions of each clinical trial, and
   also all the analysis data from each of the clinical trials, to a
   Microsoft Excel file. All clinical trial descriptions are written to
   one worksheet in the file, and all analysis data is written to a
   second worksheet in the file.

mRNA Analysis Tab
^^^^^^^^^^^^^^^^^

The mRNA Analysis tab contains gene expression data derived largely from
external experiments and from some internal experiments.

Click the **mRNA Analysis** tab to display the results in this category.
The buttons in the following figure appear at the top of the results
list. You may see fewer buttons, depending on the results of your
particular search:

|image32|

These buttons give you access to the following views and operations:

-  **Show Filters** – Define additional filters to further refine the
   search results.

-  **Analysis View** – View the analyses of the experiments that are
   ranked as statistically significant analyses.

-  **Study View** – View the details of the experiments and, optionally,
   *all* the analyses for each experiment – that is, those analyses that
   are considered statistically significant and those that are not.

-  **Export Results** – Export descriptions of each experiment, and also
   all the analysis data from each of the experiments, to a Microsoft
   Excel file. All descriptions of experiments are written to one
   worksheet in the file, and all analysis data is written to a second
   worksheet in the file.

The following sections describe the results of experiments for the
disease\ **Brain Diseases**. Click the **mRNA Analysis** tab to see the
results.

Show Filters
''''''''''''

Click the **Show Filters** button to further refine the search results.
When you click the button, a window containing filter fields appears
(shown below), and the **Show Filters** button is replaced by the **Hide
Filters** button.

In the figure below, filter selections are set for the broadest possible
search.

#. To narrow the search:
#. Specify one or more filters – for example, specify a particular
      p-value to search against, and/or select a particular species from
      the dropdown list.
#. Click **Filter Results** to start the search.

|image33|

Analysis View
'''''''''''''

Click the **Analysis View** button to view the statistically significant
analyses associated with mRNA experiments.

For information on the rules that determine how analysis results are
ranked, see *TEA Analyses* .

|image34|

When you click the **+** icon (|image35|) to pull down the list of
biomarkers, you see two arrows next to each biomarker name. The arrows
have the following meanings:

-  The leftmost arrow indicates whether the gene in the signature or
   list is up-regulated (up arrow) or down-regulated (down arrow).

-  The rightmost arrow (not shown above) indicates whether the gene in
   the comparison set is up-regulated (up arrow) or down-regulated (down
   arrow).


.. note:: The leftmost arrow has meaning only for searches involving gene signatures or lists. The arrow is not shown for other searches.


Each analysis also includes the following download option:

-  **Excel** – Download detailed analysis data (such as probe set, fold
   change ratio, p‑value) to a Microsoft Excel spreadsheet.

Study View
''''''''''

Click the **Study View** button to view the mRNA experiments that are
returned and, optionally, *all* the analyses for each experiment – that
is, those analyses that are considered statistically significant and
those that are not.

|image37|

#. To drill down from the list of experiments:
#. Click the **+** icon (|image38|) to the left of the experiment
      name to pull down a list of all the analyses done for the
      experiment.

The analysis list is similar to the list of the statistically
significant analyses in the Analysis View. However, because Study View
includes analyses ranked as not statistically significant, TEA scores
and the designations co-regulated and anti-regulated are not specified
for the analyses in Study View.
#. Click the **+** icon (|image39|) to the left of the **BioMarker**
   label to pull down a list of applicable biomarkers for an analysis.
   Note that the same export options for biomarkers are available in
   Study View as in Analysis View.

Export Results in Analysis View or Study View
'''''''''''''''''''''''''''''''''''''''''''''

While in either Analysis View or Study View, click the **Export
Results** button to export the results data in the view to a Microsoft
Excel spreadsheet:

|image40|

The Export function writes the following information to the spreadsheet:

-  Descriptions of each experiment returned from the search. This is the
   same information that appears in a details box for an experiment. In
   addition, associated diseases are exported to the Excel file.

-  Information about the analyses associated with each experiment
   returned from the search. Information includes:

   -  Analysis information displayed in the search results – for
      example, analysis description, TEA score, the list of matching
      biomarkers, and the probe set, fold change value, p-value, and TEA
      p-value associated with each biomarker.

   -  Additional information about an analysis, such as QA criteria,
      analysis platform, descriptions of the biomarkers, biomarker type
      (such as gene expression), and associated diseases involved in the
      experiment.

All descriptions of experiments are written to one worksheet in the
file, and all analysis data is written to a second worksheet in the
file.

Export Information about a Particular Analysis
''''''''''''''''''''''''''''''''''''''''''''''

To export details about all the biomarkers in a particular analysis,
click the **Excel** button to the right of the analysis name – for
example:

|image41|

Note that the number of genes shown in parentheses after the
**BioMarkers** label (16995 in the above example), which specifies the
number of genes included in the analysis, may be less than the number of
rows written to the spreadsheet. The Export function writes one row of
data for each *probe set*, not each gene, and the same gene may be
associated with multiple probe sets.

Mouse Gene Homology in Search Results
'''''''''''''''''''''''''''''''''''''

Searches can return experiment results involving mouse genes. If
experiment data is collected on a human gene and the corresponding mouse
gene, a search against a human gene may potentially return results
containing both human and mouse gene expression experiments.

For example, information on both can be found by clicking the **Export
Results** button in the search results. The **Organism** column in the
Excel worksheet indicates whether a particular measurement was made on a
human gene or a mouse gene.

The following figure shows part of an Excel worksheet containing the
results of a search against the MET gene:

|image42|

Additional Resources
''''''''''''''''''''

An mRNA Analysis search result contains links to the following
resources:

+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| Resource Link     | Description                                                                                                                             |
+===================+=========================================================================================================================================+
| Experiment name   | View information about the experiment, including title, description, and primary investigator.                                          |
|                   |                                                                                                                                         |
| Example:          | The display may contain links to additional information, such as NCBI GEO and ArrayExpress data.                                        |
|                   |                                                                                                                                         |
| |image43|         |                                                                                                                                         |
+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| QA criteria       | View key parameters of the experiment, such as p-Value and fold-change cutoffs, analysis platform, and methodology.                     |
|                   |                                                                                                                                         |
| Example:          |                                                                                                                                         |
|                   |                                                                                                                                         |
| |image44|         |                                                                                                                                         |
+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| Gene              | Search the following sites for information about the gene:                                                                              |
|                   |                                                                                                                                         |
| Example:          | |image46|                                                                                                                               |
|                   |                                                                                                                                         |
| |image45|         |                                                                                                                                         |
+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
| |image47|         | Export data (such as gene, probe set, and fold-change ratio) for the matching biomarkers in a particular analysis to Microsoft Excel.   |
+-------------------+-----------------------------------------------------------------------------------------------------------------------------------------+

Literature Tab
^^^^^^^^^^^^^^

This result category contains hits from a set of curated articles within
a set of selected diseases.

Click the **Literature** tab to display the results in this category.
The following figure shows the controls that appear at the top of the
results list.

These controls give you access to the following views and operations:

-  **Show Filters** button – Define additional filters to further refine
   the search results.

-  **Export Results** button – Write curation data to Microsoft Excel.

-  **Results for** dropdown – Specify the type of literature results you
   want to see in the categories.

Documents Tab
^^^^^^^^^^^^^

The search results in this category are based on internal text-indexed
document repositories.

TEA Analyses
------------

Target Enrichment Analysis (TEA) measures the enrichment of a gene
signature, gene list, or pathway in a microarray expression experiment.


.. note:: For information on how TEA scores are calculated, see *Appendix A: How TEA Scores Are Calculated* .


TEA Indicators Applied to Individual Biomarkers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Study View of mRNA Analysis search result lists all experiments that
satisfy the search criteria. Further, in Study View, you can list:

-  All of an experiment’s analyses that satisfy the search criteria

-  All of an analysis’ biomarkers that satisfy the search criteria

To drill down to the matching analyses in an experiment, click the **+**
icon (|image49|) next to the experiment name. To drill down to the
matching biomarkers in an analysis, click the **+ **\ icon next to the
label **BioMarkers** under the analysis name.

The following example shows the experiment **GSE4226**\ in Study View.
The biomarkers for the analysis **DiseaseState => Sporadic Alzheimer\_s
Disease vs Normal elderly control** are displayed:

|image50|

Notice the rightmost column of biomarker values: **TEA p-Value**. These
normalized p‑values are intermediate values in the TEA calculation. To
be considered a statistically significant analysis, an analysis must
have at least one matching biomarker with a TEA p-Value of less than
0.05.

The following figure shows the same experiment and analysis from the
figure above, but in Analysis View:

|image51|

Statistically significant analyses are candidates for display in the
Analysis View, after further TEA calculations are performed to determine
whether the analysis is a **significant TEA analysis** or an
**insignificant TEA analysis**.

TEA Indicators Applied to an Analysis
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The TEA algorithm assigns an aggregate score to each analysis within an
experiment. A TEA score is a binomial distribution of normalized
p-values, calculated in the context of the following factors:

-  **With gene signatures and gene lists** – The level of co-regulation
   or anti-regulation of the genes within the gene signature or gene
   list, as compared with the experiment.

-  **With pathways –** The level of up-regulation or down-regulation of
   the genes within the pathway, as compared with the experiment.


.. note:: For details on the TEA algorithm, see *Appendix A: How TEA Scores Are Calculated* .


TEA identifies experiments where the genes in the signature, list, or
pathway are *differentially modulated*, indicating that the target is
affected by the treatment, disease or other topic examined in the
experiment.

What the TEA Score Means
^^^^^^^^^^^^^^^^^^^^^^^^

The TEA score displayed for an analysis of an experiment is not the
actual TEA score calculated by the TEA algorithm. TEA scores are
typically very small decimal numbers that are not easily human-readable.
To aid users in interpreting the relative value of TEA scores, scores
are converted to a larger number, as follows:

Displayed\_TEA\_Score = -log(Actual\_TEA\_Score)

The larger the displayed TEA score, the more statistically significant
is the analysis.

Typically, displayed TEA scores for statistically significant analyses
of experiments range from 3 to 30 or 40.

Analyses of experiments are grouped into the categories **Significant
TEA Analyses** and **Insignificant TEA Analyses**, as follows:

-  Significant TEA analyses have a displayed TEA score of >= 2.9957.

-  Insignificant TEA analyses have a displayed TEA score of < 2.9957.

What Co-/Anti-Regulation and Up-/Down-Regulation Mean
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

An analysis of a statistically significant experiment returned from a
search against a gene signature or list is designated as *co-regulated*
or *anti-regulated*. An analysis of a statistically significant
experiment returned from a search against a pathway is designated as
*up-regulated* or *down-regulated*.

The following table describes what these terms imply in the context of
an analysis of a statistically significant experiment:

+----------------------+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
|                      | Gene Signature/List                                                                                          | Pathway                                                     |
+======================+==============================================================================================================+=============================================================+
| Co-Regulated         | Genes that are up-regulated in the signature or list are predominantly up-regulated in the experiment.       | n/a                                                         |
|                      |                                                                                                              |                                                             |
|                      | Genes that are down-regulated in the signature or list are predominantly down-regulated in the experiment.   |                                                             |
+----------------------+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| Anti-Regulated       | Genes that are up-regulated in the signature or list are predominantly down-regulated in the experiment.     | n/a                                                         |
|                      |                                                                                                              |                                                             |
|                      | Genes that are down-regulated in the signature or list are predominantly up-regulated in the experiment.     |                                                             |
+----------------------+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| Up-Regulated         | n/a                                                                                                          | Genes in the experiment are predominantly up-regulated.     |
+----------------------+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+
| **Down-Regulated**   | n/a                                                                                                          | Genes in the experiment are predominantly down-regulated.   |
+----------------------+--------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------+

TEA Indicators Applied to an Individual Gene
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In an analysis list, TEA indicators for a gene appear as arrows, as
shown in the figure below. The leftmost arrow represents the gene
expression in the gene signature or list. The rightmost arrow represents
the gene expression in the experiment:

|image53|


.. note:: The leftmost arrow appears only for gene signatures and gene lists.


The direction of the arrows indicates the following:

-  **Up-arrow** – An upward-pointing arrow alongside a gene indicates
   that the gene is up-regulated in the gene signature/list (leftmost
   arrow) or in the experiment (rightmost arrow).

If both arrows point in the same direction, the gene is co-regulated in
the signature/list and the experiment. If the arrows point in opposite
directions, the gene is anti-regulated.

-  **Down-arrow** – A downward-pointing arrow alongside a gene indicates
   that the gene is down-regulated in the gene signature/list (leftmost
   arrow) or in the experiment (rightmost arrow).

If both arrows point in the same direction, the gene is co-regulated in
the signature/list and the experiment. If the arrows point in opposite
directions, the gene is anti-regulated.

The relationships between TEA indicators for genes and TEA indicators
for an experiment are as follows:

-  **Co-regulated genes** – Up- or down-regulated genes in the
   signature/list are similarly up- or down-regulated in the experiment.

-  **Anti-regulated** **genes** – Up- or down-regulated genes in the
   signature/list are conversely down- or up-regulated in the
   experiment.
