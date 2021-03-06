Getting Started with tranSMART
==============================

The tranSMART application reflects the efforts of various informatics
groups to integrate data from internal and external data sources within
a single data warehouse, and to provide scientific end users the tools
to search for, view, and analyze the data in the warehouse.

The core internal data is a historical base of biomarker data from gene
expression, RBM, and SNP experiments, including both raw and analyzed
data.

External data sources include publicly available resources such as the
Gene Expression Omnibus repository and MeSH Ontology.

The tranSMART application presents scientists with a search tool to
query this vast ocean of disparate data through a Google-like user
interface.

As users become more sophisticated in developing patterns of search
terms, they can save and share their efforts with fellow researchers. A
second tool, called the Dataset Explorer, allows the properly authorized
user to create and study cohorts of patients that have been involved in
completed clinical research efforts. Dataset Explorer also provides the
user with tools to compare an individual (or group) in one study against
a person or cohort in another study.

.. note:: There may be some minor differences between the UI objects illustrated in this guide and the ones you see on your screen.


Feature Overview
----------------

tranSMART contains the following major features:

-  Search tool

-  Dataset Explorer

-  Gene Signature Wizard

Search Tool
~~~~~~~~~~~

tranSMART provides a Google-like search tool that lets you search across
multiple data sources for information related to items of interest, such
as biomarkers, diseases, genes, and gene signatures.

The scope of a search can include clinical studies, externally conducted
experiments, and in vivo/in vitro studies.

Search tool functionality includes:

-  Searching within a particular category, such as diseases, genes, or
   pathways, or searching across all categories.

-  Building complex search criteria that let you precisely define what
   to search for.

-  Saving search criteria for easy recall and re-execution.

-  Emailing search criteria to colleagues.

Search Results
^^^^^^^^^^^^^^

In searches of experiments, tranSMART displays complete listings of all
analyses related to the experiments that are found.

tranSMART flags “meaningful” results in the analysis lists. Meaningful
analyses are those where the signature genes are differentially
modulated in a statistically significant way, indicating that the
associated target is probably affected by the treatment, disease or
other topic examined in the experiment.

Search result functionality includes:

-  Displaying details of a particular experiment by clicking the name of
   the trial or experiment in the results list.

-  Accessing a number of gene-related sites – Entrez Gene, Entrez
   Global, GeneCards, and Google Scholar – by clicking the name of a
   gene in the results list.

-  Viewing the technical report or protocol used for an analysis.

-  Exporting the complete results list to a Microsoft Excel file.

-  Exporting details of a particular study, experiment, or other result
   to a Microsoft Excel file.

Dataset Explorer
~~~~~~~~~~~~~~~~

The Dataset Explorer, originally based on an i2b2 design, lets you
compare two sets of study groups based on one or more points of
comparison. You define both the criteria that populate the study groups
and the points of comparison between the study groups.

Dataset Explorer uses a standard navigation tree interface to display
data from clinical trials, and also employs an intuitive drag-and-drop
functionality to help you build the criteria for populating the study
groups and to add the points of comparison.

Dataset Explorer functionality includes:

-  Saving the criteria used to populate the study groups.

-  Emailing the study group criteria to colleagues.

-  Using a heatmap to visualize the change in the expression of a
   specific protein from one sample to another.

-  Using principal component analysis (PCA) to reduce the dimensionality
   of the dataset and to identify new, meaningful variables in the
   dataset.

-  Performing advanced analyses and displaying results in various
   formats (scatter plot with linear regression, box plot with analysis
   of variance, etc.)

-  Exporting a study or subset of a study to analyze in an external
   tool.

Gene Signature Wizard
~~~~~~~~~~~~~~~~~~~~~

tranSMART provides a wizard to help you create and define gene
signatures and gene lists.

You can use your gene signature or gene list in tranSMART searches to
find studies where the differentially regulated genes match those in
your gene signature or list. This can help you develop hypotheses about
diseases or treatments that may have similar genes deregulated.

Stored gene signatures can also be used in the analyses functionality of
Dataset Explorer.

Gene signature functionality includes:

-  Keeping the gene signature or list private so that only you can
   access it and use it in searches, or making it publicly available to
   all tranSMART users.

-  Cloning an existing gene signature or list – either yours or a public
   one – as the starting point for creating and defining a new gene
   signature or list.

-  Exporting all details of a gene signature or list to a Microsoft
   Excel file.

Logging In
----------

To log into tranSMART:

#. Type the address of the tranSMART software into your browser’s URL field (e.g. ``http://transmart.host.com/transmart``).

#. The login screen appears:

   .. image:: /media/image3

#. Type your tranSMART login credentials, then click **Login**.

.. note:: Your tranSMART software may also be configured to login
   automatically as a guest user.


Tools
-----

tranSMART provides the following tools:

-  **Search** – Search across internal and external data sources for
   research data and literature related to search terms that you
   provide.

-  **Dataset** **Explorer** – View study data for subjects that you
   select, based on criteria that you specify. Also, compare data
   generated for subjects in two different study groups, based on
   criteria and points of comparison that you specify.

-  **Gene** **Signature/Lists** – View definitions of existing gene
   signatures and add new gene signature definitions.

-  **Utilities** – contains the following submenus:

   -  **Help** – Display links to the tranSMART documentation set.

   -  **Contact Us –** Email questions, problem reports, enhancement
      requests, or any other feedback about the tranSMART application.

   -  **About** – Displays the version of tranSMART.

Select the tranSMART tool to use by clicking one of the tool tabs at the
top of the tranSMART window:

.. image:: /media/image5


Opening a Particular Tool at Login
----------------------------------

By default, tranSMART opens the Search tool after you log in. However,
you can specify the tool for tranSMART to open immediately after login
by including the tool name in the address you type into your browser’s
URL field.

To automatically open a particular tranSMART tool immediately after
login, use an address listed below:

-  Search tool – either of the following::

      https://transmart.host.com/transmart

      https://transmart.host.com/transmart/search

-  Dataset Explorer tool::

      https://transmart.host.com/transmart/datasetExplorer

-  Gene Signature/Lists tool::

      https://transmart.host.com/transmart/geneSignature

.. note:: The addresses above are case-sensitive. Also, this (and future examples) use the tranSMART instance address ``https://transmart.host.com``. Substitute the address of your local instance.
