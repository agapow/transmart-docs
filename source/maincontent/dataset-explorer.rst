Dataset Explorer
===========================

Dataset Explorer lets you compare data generated for test subjects in
two different study groups, based on criteria and points of comparison
that you specify. Dataset Explorer is useful to help you test a
hypothesis that involves the criteria and points of comparison that you
select.

Overview of the UI
------------------

The figure below shows the Dataset Explorer interface. It is divided
into two panes:

**Left pane**

-  Lets you select the study of interest.

-  Provides a navigation tree where you select the criteria for
   membership in the study groups and the points of comparison between
   the study groups.

**Right pane **

-  Lets you define the criteria that test subjects must satisfy to
   become members of one of the two groups being compared. Each of these
   groups is called a *subset* because it typically contains only some
   of the subjects in the actual study group involved in the study.

You define the criteria for the subsets in the subset definition boxes
shown below. Subjects who do not satisfy the criteria you define are
excluded from the subsets.

-  Provides summary data about the subjects being compared, and several
   different views of the comparison data.

    |image55|

The following table describes the buttons and tabs in the right pane of
Dataset Explorer:

+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Button or Tab                        | Description                                                                                                                                                                                               |
+======================================+===========================================================================================================================================================================================================+
| Generate Summary Statistics button   | Displays tables and charts that describe demographic information about the subjects in the subsets, and also analyses of criteria included in the subset definitions.                                     |
|                                      |                                                                                                                                                                                                           |
|                                      | The tables and charts are displayed in the Results/Analysis view.                                                                                                                                         |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Summary button                       | Displays a summary of the query criteria you specified. Dataset Explorer uses these criteria to select the subjects for the subsets.                                                                      |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Clear button                         | Clears all the criteria in the subset definition boxes.                                                                                                                                                   |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Save button                          | Saves the criteria definition. This allows you to re-generate the comparison at a later time without having to reconstruct the criteria that select the subjects for the subsets.                         |
|                                      |                                                                                                                                                                                                           |
|                                      | For more information, see *Saving Comparison Definitions* .                                                                                                                                     |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Export button                        | Exports summary statistics data or expression data to Microsoft Excel.                                                                                                                                    |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Print button                         | Prints the tables and charts in the Results/Analysis view.                                                                                                                                                |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Comparison tab                       | Removes the currently displayed view (that is, the Results/Analysis view, or Grid view) and re-displays the subset definition boxes. This allows you to further refine the subjects for the comparison.   |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Advanced Workflow tab                | Displays advanced analyses and visualizations that you can perform on data.                                                                                                                               |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Results/Analysis tab                 | Displays tables and charts containing comparison and analysis data generated from the “Summary Statistics” workflow.                                                                                      |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Grid View tab                        | Displays the comparison and analysis data in grid format.                                                                                                                                                 |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Jobs tab                             | Displays previously run analyses.                                                                                                                                                                         |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Data Export tab                      | Allows you to select data to export for further analysis in an external tool.                                                                                                                             |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Export Jobs tab                      | Displays previously exported jobs.                                                                                                                                                                        |
+--------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Using Dataset Explorer
----------------------

Four basic tasks are involved in using Dataset Explorer:

-  Select the study (clinical trial or experiment) to use in the
   comparison.

-  Specify the criteria for membership in the two study groups. Note
   some analyses only allow for the specification of one group at this
   time.

-  Generate summary statistics for the two study groups.

-  Specify the points of comparison to apply to the study groups.


.. note:: You may see the notations **NA** and **Unknown** in the study data. **NA** indicates not applicable, and **Unknown** indicates not available.


Public and Private Studies
~~~~~~~~~~~~~~~~~~~~~~~~~~

Dataset Explorer studies can be either public or private. Public studies
can be found both in the **Public Studies** folder of the Dataset
Explorer navigation tree, as well as in the research-specific folders.

You can perform all the operations described in this chapter on public
studies. No special privileges are required.

To perform operations described in this chapter on a private study, a
tranSMART Administrator must assign you access rights to the study.
Access rights are based on the following access levels:

+----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Access Level   | Privileges                                                                                                                                                          |
+================+=====================================================================================================================================================================+
| VIEW           | Define the criteria for the study groups to be compared, generate summary statistics for the study groups, and specify points of comparison for the study groups.   |
+----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| EXPORT         | All privileges of the VIEW access level, plus the ability to export comparison data or expression data to a Microsoft Excel spreadsheet.                            |
+----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| OWN            | All VIEW and EXPORT privileges.                                                                                                                                     |
|                |                                                                                                                                                                     |
|                | This access level can only be assigned to the owner of the study.                                                                                                   |
+----------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------+

If you do not have access rights to the study you want (that is, if the
study name is grayed out), contact a tranSMART Administrator. The
administrator will contact the study owner to find out if you should be
granted VIEW access, EXPORT access, or no access.


.. note:: Even if you have no access rights to a private study, you can read a description of the study. For information, see *Viewing a Study* .


Selecting the Study
~~~~~~~~~~~~~~~~~~~

You select the study in the left pane of Dataset Explorer. You have
several ways to select the study, based on the tab you choose – Search
Terms or Navigate Terms.

Search Terms Tab
^^^^^^^^^^^^^^^^

Use this tab to search for studies using one or a combination of the
following fields:

-  **Search** field. It lets you specify part or all of a term from a
   study that is stored in the tranSMART database. Search terms may
   include part or all of a study name, the text in a branch of the
   Dataset Explorer navigation tree, or some attribute of a study, such
   as a disease or an area of clinical interest.

Example:

|image58|

If you want to base your search on a study name, note the following
naming conventions for Public Studies in Dataset Explorer:

+------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Study Type       | Naming Convention                                                                                                                                                                                 |
+==================+===================================================================================================================================================================================================+
| Public Studies   | Name segments in the following typical format:                                                                                                                                                    |
|                  |                                                                                                                                                                                                   |
|                  | *Condition\_StudyFirstAuthor*\ \_\ *GEOid*                                                                                                                                                        |
|                  |                                                                                                                                                                                                   |
|                  | Example: ProstateCancer\_Ambs\_GSE6956                                                                                                                                                            |
|                  |                                                                                                                                                                                                   |
|                  | If you prefer, you can rearrange the order of the segments (for example, author segment first). The name structure is determined by the ETL process that loads the data into the i2b2 database.   |
+------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Selecting and Opening a Study in a Search Result
''''''''''''''''''''''''''''''''''''''''''''''''

A search result may include multiple entries. Further, an entry may not
indicate the study it is from. To see the name of the study that an
entry represents, hover the mouse pointer over the entry – for example:

|image59|

If you want more information about the study represented by an entry,
right-click the entry, then click **Show** **Definition** to open the
details box for the study:

|image60|

To open a study from an entry in a search result, right-click the entry,
then click **Show** **Node**. The study appears in the Dataset Explorer
navigation tree, where you can open any of the branches (nodes) in the
study.


.. note:: You may need to scroll down slightly in the navigation tree to see the study.


Navigate Terms Tab
^^^^^^^^^^^^^^^^^^

Use this tab to browse through all the experiments in the navigation
tree to select and open the study you want.

Studies that are grayed out are private studies that you are not
authorized to access.

To display the details box for a study, right-click the study name and
click **Show** **Definition**. You can display the details box for a
study whether or not the study is grayed out.

Branches and Leaves of the Navigation Tree
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Dataset Explorer navigation tree looks and works much likeyour
operating system’s file explorer: it is a an expandable hierarchy of
folders, sub-folders, and files. Dataset Explorer is a hierarchy of
folders and sub-folders (the branches) and values (the leaves) that
reflect aspects of the trial, such as research metrics, compounds used,
and patient demographics.

In Dataset Explorer, all levels of the tree, both branches and leaves,
are referred to as nodes.

The following figure shows typical top-level nodes of a study. Some
studies may not require all of these nodes, and others may require
additional nodes (such as Published Conclusions):

|image62|

The following table describes possible top-level nodes of a study:

+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Node                     | Description                                                                                                            |
+==========================+========================================================================================================================+
| Biomarker Data           | Measurements of biomarkers such as RBM antigens, gene expressions, antibodies and antigens in ELISA tests, and SNPs.   |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Clinical Data            | Primary and secondary endpoints, and other measurements from the study.                                                |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Samples and Timepoints   | Tested samples (such as tissue or blood) and time periods when the samples were taken.                                 |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Scheduled Visits         | Periodic stages of the trial during which patients are seen.                                                           |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Design Factors           | Compounds involved in the study, dosages, and regularity with which the compounds were administered.                   |
|                          |                                                                                                                        |
|                          | **Note:** With clinical trials, this node is typically named Treatment Groups.                                         |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+
| Sample Factors           | Patient information, such as demographics and medical history.                                                         |
+--------------------------+------------------------------------------------------------------------------------------------------------------------+

Populating the Study Groups
~~~~~~~~~~~~~~~~~~~~~~~~~~~

You populate the study groups by defining criteria that members of each
group must satisfy. For example, members of study groups might be
required to satisfy a weight or age requirement. Dataset Explorer lets
you build a set of criteria for each study group that can be as simple
or as complex as you need.

The study groups you define are called *subsets*, because typically,
after your criteria are applied, the members of a resulting study group
are a subset of the full study group that participated in the study.

Selecting Criteria for the Study Groups
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You define the study groups by selecting criteria (called concepts) from
the navigation tree and dragging them into the subset definition boxes.

Visual Aids to Help You Select the Criteria
'''''''''''''''''''''''''''''''''''''''''''

Each concept node in the navigation tree displays the following
information about the concept:

-  The numbers in parentheses at each node of the tree indicate the
   number of subjects to whom that node applies. For example, in the
   figure below, there are a total of 327 subjects in the study.

-  In tranSMART, data values are represented in one of three ways: by
   number, by text, or by high dimensional data (SNP, gene expression,
   etc.) stored as *arrays*.

   The three types of data values are described in the illustration
   below:

   |image63|

Specifying a Numeric Value
^^^^^^^^^^^^^^^^^^^^^^^^^^

When you drag a numeric concept into a subset definition box, the Set
Value dialog appears:

|image64|

Use the Set Value dialog to specify how you want to constrain the
numeric values to use in the subset definition. To do so, first select
one of the following choices:

+--------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Selection          | Description                                                                                                                                                                  |
+====================+==============================================================================================================================================================================+
| No Value           | Values are not constrained. All the numeric data associated with the concept are factored into the subset definition.                                                        |
|                    |                                                                                                                                                                              |
|                    | If you select **No Value**, no other information is required. Click **OK** to add the concept with all its associated numeric data to the subset.                            |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| By high/low flag   | If the testing laboratory has grouped the numeric values into high/low/normal ranges, select the range to factor into the subset definition.                                 |
|                    |                                                                                                                                                                              |
|                    | When you select **By high/low flag**, the **Please select range** field appears. Select the range you want and click **OK**.                                                 |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| By numeric value   | Values are constrained by an exact value or a range of values.                                                                                                               |
|                    |                                                                                                                                                                              |
|                    | After you select **By numeric value**:                                                                                                                                       |
|                    |                                                                                                                                                                              |
|                    | -  Select one of the following numeric operators in the **Please select operator dropdown**:                                                                                 |
|                    |                                                                                                                                                                              |
|                    | |image65|                                                                                                                                                                    |
|                    |                                                                                                                                                                              |
|                    | -  In **Please enter value**, type the numeric value that the operator applies to.                                                                                           |
|                    |                                                                                                                                                                              |
|                    | For example, to constrain the ages of subjects to 50 years or younger, select LESS THAN OR EQUAL TO(<=) in the dropdown, then type 50 in the **Please enter value** field.   |
|                    |                                                                                                                                                                              |
|                    | -  Click **OK.**                                                                                                                                                             |
|                    |                                                                                                                                                                              |
|                    | See the next section for information on viewing the numeric values associated with the concept and that you can select from.                                                 |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


.. note:: When finished defining the numeric constraint on the Set Value dialog, be sure to click **OK** and not press the **Enter** key. Pressing **Enter** will activate the subset button that has focus – the **Exclude** button in the example below:


|image67|

Viewing the Numeric Values Associated with a Concept
''''''''''''''''''''''''''''''''''''''''''''''''''''

Note the buttons **Show Histogram** and **Show Histogram for subset** in
the Set Value dialog. The histograms show how the numeric values
associated with the concept that you placed in the subset box are
distributed among the subjects across both subsets, or in the particular
subset you are currently defining, respectively.

A histogram may be helpful in determining the number to set as the
constraining factor for a concept. For example, suppose you drag a
Weight concept into a subset box, then click **Show Histogram for
subset**. In the following histogram of the weights of test subjects,
the weights range from about 25 kg to just under 125 kg. The largest bin
represents just under 50 subjects. You may want to use these weight
parameters to help you determine the value to set for the weight
concept.

|image68|

You can get more specific information about the number of subjects
represented by a particular bin and the average of the values in the bin
by hovering the mouse cursor over the bin you are interested in. For
example, in the following figure, the largest bin represents 49 subjects
with an average weight of 68.7 kg:

|image69|

Saving Comparison Definitions
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You may save your search criteria in order to regenerate the comparison
at a later time without having to redefine the subsets.

#. To save search criteria:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Select the study of interest.
#. Define the cohorts whose data points will be represented.
#. Click **Save**:

      |image70|
#. Click **Email this comparison**:

      |image71|

Your email application will open with a link to the saved comparison.
#. Send the email to yourself so that you can retrieve the comparison
   later. Optionally, send it to colleagues who might be interested in
   the comparison.

When you or someone else clicks the link in the email, Dataset Explorer
opens with the subset boxes pre-defined.

Joining Multiple Criteria for a Subset Definition
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Multiple criteria for a subset definition are joined by one of the
following logical operators: AND, OR, or AND NOT.

The rules for joining multiple criteria are as follows:

-  Criteria in separate subset definition boxes are joined by an AND
   operator.

For example, the following definition boxes select only male subjects,
AND males whose weights are between 65 kg and 90 kg:

|image72|

-  Criteria within the same subset definition box are joined by an OR
   operator.

For example, to use the extreme ends of the weight scale for your weight
criterion, you might add the following to a definition box:

|image73|

This criterion selects subjects whose weight is either 50 kg or less, OR
100 kg or greater.

-  To join a definition box with an AND NOT operator, click the
   **Exclude** button above the definition box.

The figure below selects only male subjects, but not those who weigh
between 50 kg and 100 kg:

|image74|

Note that when you click the **Exclude** button, the button label
changes to **Include**, allowing you to join the criteria in the box
with an AND operator later if you choose.

Modifying or Deleting Criteria
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To delete or modify a criterion in a subset definition box, right-click
the criterion and select either **Delete** or **Set Value**.

To remove the entire contents of a subset definition box from the subset
definition, click the **X** icon (|image75|) above the box:

|image76|

Generating Summary Statistics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you finish defining criteria for the groups to compare – the
subsets – click the **Generate Summary Statistics** button.

tranSMART displays tables and charts of information that describe the
subsets. The information is displayed in the Results/Analysis view in
the following sections:

-  A summary of the criteria used to define subsets to compare. Example:

|image77|

-  A table showing the number of subjects in each subset who match the
   subset criteria. Example:

    |image78|

    In this example, 52 subjects matched the criteria for Subset 1, and
    48 matched the criteria for Subset 2. Further, 25 subjects matched
    the criteria for both subsets (and thus, were included in both).

-  Tables and charts that show how the subjects who match the criteria
   fit into age, sex, and race demographics. Example (showing the age
   portion only):

|image79|

-  Analyses of the concepts you added to the subsets from the navigation
   tree. Example (showing the weight concept):

|image80|

Significance Tests
^^^^^^^^^^^^^^^^^^

The above figure includes the results of significance testing that
Dataset Explorer performs:

|image81|

Significance testing is designed to indicate whether the reliability of
the statistics is 95% or greater, based on p-value.

Dataset Explorer calculates the significance result using either t-test
or chi-squared statistics to determine the p-value:

-  For continuous variables (for example, subject weight or age), a
   t-test compares the observed values in the two subsets.

tranSMART uses the following Java method to calculate the t-test
statistic:

    `http://commons.apache.org/proper/commons-math/apidocs/org/apache/commons/math3/stat/inference/TTest.html#tTest(double[],
    double[]) <http://commons.apache.org/proper/commons-math/apidocs/org/apache/commons/math3/stat/inference/TTest.html#tTest(double[], double[])>`__

-  For categorical values (for example, diagnoses), a chi-squared test
   compares the counts in the two subsets.

tranSMART uses the following Java method to calculate the chi-squared
statistic:

    `http://commons.apache.org/proper/commons-math/apidocs/org/apache/commons/math3/stat/inference/ChiSquareTest.html#chiSquareTest(long[][]) <http://commons.apache.org/proper/commons-math/apidocs/org/apache/commons/math3/stat/inference/ChiSquareTest.html#chiSquareTest(long[][])>`__

If there is not enough data to calculate a test, Dataset Explorer
displays a message indicating the insufficient quantity data. Also,
significance test results are not displayed in the following
circumstances:

-  If two identical subsets are defined. In this case, the significance
   test results are not meaningful.

-  If all subjects in the first subset have one set of values for the
   categorical value, and all subjects in the second subset have other
   categorical values. For example, suppose you set Subset 1 to contain
   only males and Subset 2 to contain only females. Also, suppose that
   Subset 1 has 15 subjects and Subset 2 has 20. If you then try to show
   statistics by gender, a table like the following would result:

+----------+------------+------------+
|          | Subset 1   | Subset 2   |
+==========+============+============+
| Female   | 0          | 20         |
+----------+------------+------------+
| Male     | 15         | 0          |
+----------+------------+------------+

In this case, the chi-squared function doesn’t return meaningful
results.

Defining Points of Comparison
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you establish the subsets of subjects that you want to compare, you
can apply one or more points of comparison to the subsets.

A point of comparison is a concept in the navigation tree.

#. To apply a point of comparison to the subsets:
#. You must already have defined the subsets and have generated
      summary statistics for the subsets, as described in the previous
      section.
#. Drag the concept that you want to introduce as the point of
      comparison from the navigation tree, and drop it anywhere in the
      Results/Analysis view.

As soon as you drop the point of comparison into the Results/Analysis
view, tranSMART begins to compare the subsets based on that point of
comparison. When finished, tranSMART displays a side-by-side summary of
how the subjects in each subset match or respond to the point of
comparison.

Results of a Comparison
^^^^^^^^^^^^^^^^^^^^^^^

In a comparison of subjects in a psychological study, suppose Subset 1
contains subjects with a substance abuse problem, and Subset 2 contains
subjects with no substance abuse assessment.

After the subsets are defined and summary statistics are generated, a
diagnosis of depression is dropped into the Results/Analysis view as a
point of comparison. tranSMART displays a side-by-side comparison of the
subjects in each subset, indicating that almost all the subjects with a
substance abuse problem have been diagnosed with depression, while that
diagnosis for those with no substance abuse problem is more evenly
split.

The comparison is placed at the top of the Results/Analysis view, above
the demographic definitions plus any other earlier comparisons:

|image82|


.. note:: To keep the size of the preceding figure within production limits, the demographics (age, sex, and race) portions of the figure have been excluded.


Printing or Saving the Contents of the Results/Analysis View
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#.
#. With the Results/Analysis view displayed, click **Print**:

|image84|

The entire contents of the Results/Analysis view appear in a separate
browser window.
#. Click one of the following buttons at the top of the browser window:

|image85|

Copying Individual Charts in the Results/Analysis View
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you are interested in a particular chart in the Results/Analysis
View, you can copy the chart to a file, as follows:

#.
#. With the Results/Analysis view displayed, click **Print**.

The entire contents of the Results/Analysis view appear in a separate
browser window.
#. Right-click the chart to copy.
#. In the browser popup menu, click **Save Image As**.
#. In the Save Picture dialog, specify the name, location, and the file
   type for the chart.
#. Click **Save**.

Viewing a Study
---------------

You can view a description of any Dataset Explorer study, whether or not
you have access rights to the study.

#. To view a description of a study:
#. In Dataset Explorer, click the **Navigate Terms** tab.
#. Open the top-level node for the list of studies you are interested
      in – for example, click the **+** icon (|image86|) next to Public
      Studies to open the list of experiments:

|image87|
#. Right-click the particular study you are interested in.
#. Click the **Show Definition** popup:

|image88|

The Show Concept Definition dialog appears, showing the title,
description, and other information about the study.

Exporting Dataset Explorer Findings
-----------------------------------

The Data Export tab allows you to export your data locally for further
analysis in several different formats. Exporting data using this tool
involves the following high-level tasks:

|image89|

Supported file formats include:

-  Clinical and low dimensional biomarker data

-  Gene expression data

-  SNP data

-  Gene set enrichment analysis (GSEA)


.. note:: For more information on GSEA data files, visit the following site: *http://www.broadinstitute.org/cancer/software/gsea/wiki/index.php/   |
|             | Data\_formats*


#. To export Dataset Explorer findings to your local machine:
#. Click the tranSMART **Dataset Explorer** tab to display the
      Dataset Explorer window.
#. In the left pane of the Dataset Explorer window, click the
      **Navigate Terms** tab.

      The navigation tree appears, showing the categories of available
      studies:

      |image91|
#. Select the study of interest.
#. Define the cohorts whose data points are of interest.

      Now that the subsets are defined, you are ready to export data
      from the study that applies to the subsets.
#. Click the **Data Export** tab:

      |image92|

      The Data Export page appears with your selected cohorts:

      |image93|
#. Select the check boxes to indicate the data types and file formats
      that are desired for export.
#. Click **Export Data** at the bottom of the tranSMART browser
      window.

      The command will now start a job. You may choose to have the job
      run in the background in order to continue with other analyses and
      cohort selection while the job completes. The job could take
      several minutes depending on the amount of data selected.
#. Click the **Export Jobs** tab to access completed jobs or to check
      the status of a pending job.

      Jobs follow the naming convention *User - Type of Job Run - Job
      ID.*
#. Click the name of the job you processed:

      |image94|

      The Open File dialog box appears:

      |image95|
#. Select **Save File**, then click **OK**.

      Your file will be sent to the **Downloads** folder on your local
      machine in a .zip file. The .zip file contains separate folders
      for subsets, clinical data, gene expression data, and other
      factors you may have specified during cohort selection.

Generating Advanced Analyses and Visualizations
-----------------------------------------------

Advanced analyses and visualizations offered with tranSMART allow a user
to produce the following within Dataset Explorer:

-  Heatmaps

   -  *Standard Heatmap* (page 49)

   -  *Hierarchical Clustering* (page 51)

   -  *K-Means Clustering* (page 54)

   -  *Marker Selection* (page 56)

-  Advanced Analyses

   -  *Box Plot with ANOVA* (page 59)

   -  *Principal Component Analysis* (page 61)

   -  *Scatter Plot with Linear Regression* (page 64)

   -  *Survival Analysis* (page 66)

   -  *Table with Fisher Test Analysis* (page 69)

Dataset Explorer uses the R software environment for statistical
computing and to generate analyses and visualizations. For more
information, visit http://www.r-project.org.

Generating Heatmaps
~~~~~~~~~~~~~~~~~~~

In Dataset Explorer, a heatmap is a matrix of data points for a
particular set of biomarkers, such as genes, at a particular point in
time and/or for a particular tissue sample in the study, as measured for
each subject in the study.

In a Dataset Explorer heatmap, the biomarkers appear in the y axis, and
the subjects appear in the x axis.


.. note:: A heatmap can display data points for up to 1000 samples.


Dataset Explorer uses the R software environment for statistical
computing and to generate analyses and visualizations. For more
information, visit http://www.r-project.org.

You can generate the following types of heatmaps:

-  *Standard Heatmap* (below)

-  *Hierarchical Clustering* (page 51)

-  *K-Means Clustering* (page 54)

-  *Marker Selection* (page 56)

Standard Heatmap
^^^^^^^^^^^^^^^^

A standard heatmap is a visualization of biomarker data points with no
indication of patterns, groupings, or differentiation among the data
points.

#. To generate a standard heatmap:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: To compare two subsets, you may drag an additional concept into the Subset 2 comparison box.

#. Click the **Advanced Workflow** tab:

   |image98|
#. Select **Heatmap** from the **Analysis** dropdown menu:

   |image99|

   The Variable Selection section appears.
#. Define the heatmap variable by selecting a high dimensional data node
   from the Dataset Explorer tree and dragging it into the Heatmap
   Variable definition box:

   |image100|


.. note:: High dimensional data nodes are indicated by the icon (|image102|) to the left of study data.

#. Click the **High Dimensional Data** button.

   The Compare Subsets-Pathway Selection dialog appears.
#. Specify the platform and other factors of interest.

   For more information, see *High Dimensional Data* .
#. Click **Apply Selections**.
#. Click **Run**.

   Your analysis appears below:

   |image103|

Hierarchical Clustering
^^^^^^^^^^^^^^^^^^^^^^^

Hierarchical clustering is a visualization of patterns of related data
points in gene expression data.

#. To generate a hierarchical clustering heatmap:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: To compare two subsets, you may drag an additional concept into the Subset 2 comparison box.

#. Click the **Advanced Workflow** tab:

   |image105|
#. Select **Hierarchical Clustering** from the **Analysis** dropdown
   menu:

   |image106|

   The Variable Selection section appears.
#. Define the heatmap variable by selecting a high dimensional data node
   from the Dataset Explorer tree and dragging it into the Heatmap
   Variable definition box:

   |image107|


.. note:: High dimensional data nodes are indicated by the icon (|image109|) to the left of study data.

#. Click the **High Dimensional Data** button.

   The Compare Subsets-Pathway Selection dialog appears.
#. Specify the platform and other factors of interest.

   For more information, see *High Dimensional Data* .
#. Click **Apply Selections**.
#. Click **Run**.

   Your analysis appears below:

   |image110|


.. note:: To read more about Hierarchical Clustering, visit: http://www.ics.uci.edu/~eppstein/280/cluster.html


K-Means Clustering
^^^^^^^^^^^^^^^^^^

K-Means clustering is a visualization of groupings of the most closely
related data points, based on the number of groupings you specify.


.. note:: The K-Means analysis clusters columns together – rows are not clustered.


#. To generate a k-means clustering heatmap:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: To compare two subsets, you may drag an additional concept into the Subset 2 comparison box.

#. Click the **Advanced Workflow** tab:

   |image114|
#. Select **K-Means Clustering** from the **Analysis** dropdown menu:

   |image115|

   The Variable Selection section appears.
#. Define the heatmap variable by selecting a high dimensional data node
   from the Dataset Explorer tree and dragging it into the Heatmap
   Variable definition box:

   |image116|


.. note:: High dimensional data nodes are indicated by the icon (|image118|) to the left of study data.

#. Click the **High Dimensional Data** button.

   The Compare Subsets-Pathway Selection dialog appears.
#. Specify the platform and other factors of interest.

   For more information, see *High Dimensional Data* .
#. Click **Apply Selections**.
#. In the **Number of clusters** field, type a numerical value.
#. Click **Run**.

   Your analysis appears below:

   |image119|


.. note:: To read more about K-Means Clustering, visit: http://www.ics.uci.edu/~eppstein/280/cluster.html


Marker Selection
^^^^^^^^^^^^^^^^

A marker selection heatmap is a visualization of differentially
expressed genes in distinct phenotypes. Specifically, the algorithm
determines the set of genes which is most differently expressed between
the two subsets. This list of differentially expressed genes is
subsequently presented in a table, along with a variety of accompanying
statistics.

#. To generate a marker selection heatmap:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: Two subsets must be specified when using a Marker Selection heatmap.

#. Click the **Advanced Workflow** tab:

   |image122|
#. Select **Marker Selection** from the **Analysis** dropdown menu:

   |image123|

   The Variable Selection section appears.
#. Define the required variable by selecting a high dimensional data
   node from the Dataset Explorer tree and dragging it into the Marker
   Variable definition box:

   |image124|


.. note:: High dimensional data nodes are indicated by the icon (|image126|) to the left of study data.

#. Click the **High Dimensional Data** button.

   The Compare Subsets-Pathway Selection dialog appears.
#. Specify the platform and other factors of interest.

   For more information, see *High Dimensional Data* .
#. Click **Apply Selections**.

   In the **Number of Markers** field, type a numerical value. This will
   determine the number of differentially expressed genes that are
   returned.
#. Click **Run**.

   Your analysis appears below:

   |image127|


.. note:: For more information on the analyses used in Marker Selection, visit: http://mathworld.wolfram.com/BonferroniCorrection.html


Generating Advanced Analyses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Advanced analyses include:

-  *Box Plot with ANOVA* (page 59)

-  *Principal Component Analysis* (page 61)

-  *Scatter Plot with Linear Regression* (page 64)

-  *Survival Analysis* (page 66)

-  *Table with Fisher Test Analysis* (page 69)

Box Plot with ANOVA
^^^^^^^^^^^^^^^^^^^

A box plot with ANOVA analysis displays a box and whisker plot with
corresponding analysis of variance in the sample(s).

#. To perform a box plot with ANOVA analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: Only one subset may be specified in this analysis. Information in Subset 2 will be ignored.

#. Click the **Advanced Workflow** tab:

   |image130|
#. Select **Box Plot with ANOVA** from the **Analysis** dropdown menu:

   |image131|

   The Variable Selection section appears. You will need to define what
   variables in the study are independent, and what variables are
   dependent. At least one of the variables should be continuous (for
   example, Age), and one should be a categorical value (for example,
   Tissue Type).


.. note:: If the *independent variable* defines the groups, boxes will be plotted horizontally. If the *dependent variable* defines the groups, boxes will be plotted vertically.

#. Define the variables.


.. note:: In this example, the data binning feature is not used. For future reference, data binning refers to a pre-processing technique used to reduce minor observation errors. Clusters of data are replaced by a value representative of that cluster (the central value). For information on binning, see *Data Binning* .

#. Click **Run**.

   Your analysis appears below:

   |image134|

Principal Component Analysis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

In a principal component analysis (PCA), the total number of variables
in the dataset is reduced to a smaller number of variables – the
principle components of the dataset.

Principal component variables are calculated from correlated variables
in the total dataset. In other words, the principal component analysis
is a workflow used to identify variance in a dataset. The analysis can
be run on an entire microarray chip, or on a pathway.

#. To perform a principal component analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: Only one subset may be specified in this analysis. Information in Subset 2 will be ignored.

#. Click the **Advanced Workflow** tab:

   |image136|
#. Select **PCA** from the **Analysis** dropdown menu:

   |image137|

   The Variable Selection section appears.
#. Define the heatmap variable by selecting a high dimensional data node
   from the Dataset Explorer tree and dragging it into the PCA Variable
   definition box:

   |image138|


.. note:: High dimensional data nodes are indicated by the ( |image140| ) icon to the left of study data.

#. Click the **High Dimensional Data** button.

   The Compare Subsets-Pathway Selection dialog appears.
#. Specify the platform and other factors of interest.

   For more information, see *High Dimensional Data* .
#. Click **Apply Selections**.
#. Click **Run**.

   Your analysis appears below:

   |image141|


.. note:: For more information regarding PCAs, see: http://psb.stanford.edu/psb-online/proceedings/psb00/raychaudhuri.pdf.


Scatter Plot with Linear Regression
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A scatter plot displays values for two variables within a dataset, with
a line that best fits the slope of the data.

#. To perform a scatter plot with linear regression analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: Only one subset may be specified in this analysis. Information in Subset 2 will be ignored.

#. Click the **Advanced Workflow** tab above Subset 1:

   |image144|
#. Select **Scatter Plot with Linear Regression** from the **Analysis**
   dropdown menu:

   |image145|

   The Variable Selection section appears. You will need to define what
   variables in the study are independent, and what variables are
   dependent. Both variables should be continuous (for example, Age).
#. Define the variables.
#. Click **Run**.

   Your analysis appears below:

   |image146|

Survival Analysis
^^^^^^^^^^^^^^^^^

A survival analysis displays time-to-event data.

#. To perform a survival analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .
#. Click the **Advanced Workflow** tab above Subset 1:

      |image147|
#. Select **Survival Analysis** from the **Analysis** dropdown menu:

      |image148|

      The Variable Selection section appears.
#. Define the following variables:

+-------------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------+
| Variable          | Required?   | Definition                                                                                                                                                                                                      | Example                         |
+===================+=============+=================================================================================================================================================================================================================+=================================+
| Time              | Yes         | A numeric field within tranSMART.                                                                                                                                                                               | Survival at Follow Up (Years)   |
|                   |             |                                                                                                                                                                                                                 |                                 |
|                   |             |                                                                                                                                                                                                                 | |image149|                      |
+-------------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------+
| Category          | No          | A concept that is dragged into this input will dictate the groups into which the data will be split in order to compare their survival times.                                                                   | Cancer Stage                    |
|                   |             |                                                                                                                                                                                                                 |                                 |
|                   |             | If this variable is continuous, it requires binning. For details, see *Data Binning Using Survival Analysis* .                                                                                        | |image150|                      |
+-------------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------+
| Censoring Value   | No          | Specifies which patients had the event whose time is being measured. For example, if the Time variable selected is **Overall Survival Time (Years)**, an appropriate censoring variable is **Patient Death**.   | Dead                            |
|                   |             |                                                                                                                                                                                                                 |                                 |
|                   |             |                                                                                                                                                                                                                 | |image151|                      |
+-------------------+-------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+---------------------------------+

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| |image152|   | In this example, the data binning feature is not used. For future reference, data binning refers to a pre-processing technique used to reduce minor observation errors. Clusters of data are replaced by a value representative of that cluster (the central value). For information on data binning, see *Data Binning Using Survival Analysis* .   |
+==============+================================================================================================================================================================================================================================================================================================================================================================+
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
#. Click **Run**.

   Your analysis appears below:

   |image153|

Table with Fisher Test Analysis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A Fisher Test analysis examines the significance of associated
variables.

#. To perform a table with fisher test analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .


.. note:: Only one subset may be specified in this analysis. Information in Subset 2 will be ignored.

#. Click the **Advanced Workflow** tab:

   |image155|
#. Select **Table with Fisher Test** from the **Analysis** dropdown
   menu:

   |image156|

   The Variable Selection section appears. You will need to define what
   variables in the study are independent, and what variables are
   dependent. Both variables should be categorical values (for example,
   Tissue Type).


.. note:: In this example, the data binning feature is not used. For future reference, data binning refers to a pre-processing technique used to reduce minor observation errors. Clusters of data are replaced by a value representative of that cluster (the central value). For information on data binning, see *Data Binning* .

#. Define the variables.
#. Click **Run**.

   Your analysis appear below:

   |image158|

Data Binning
~~~~~~~~~~~~

Data binning refers to a pre-processing technique used to reduce
observation errors and to allow continuous variables to become
categorical. Clusters of data are replaced by a value representative of
that cluster (the central value).


.. note:: The data displayed after binning represents the data available in the study. If, for example, you have selected to bin based on date range (0-10 years of age), yet there is only data available for subjects eight years old and up, the bin will display the age range as 8-10.


Data Binning Using Box Plot with ANOVA
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When conducting a Box Plot with ANOVA analysis, at least one of the
variables selected should be a continuous variable (for example, age),
and the other should be a categorical value (for example, tumor stage).

A continuous variable can be viewed as a categorical value using the
binning feature, described below. Alternatively, binning can also be
used to categorize data. For example, if histological grade with values
such as Well Defined, Moderately Well Defined, and Poorly Defined are
selected, you can group Moderately Well Defined with Poorly Defined and
treat them as one group for the purposes of this analysis.

#. To use the data binning feature with a box plot analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .
#. Click the **Advanced Workflow** tab:

      |image160|
#. Select **Box Plot with ANOVA** from the **Analysis** dropdown
      menu:

      |image161|

      The Variable Selection section appears. You will need to define
      what variables in the study are independent, and what variables
      are dependent. At least one of the variables should be continuous
      (for example, Age), and one should be a categorical value (for
      example, Tissue Type).
#. Define the variables.
#. Under **Binning**, click **Enable**:

      |image162|
#. Define the following:

+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Field             | Description                                                                                                     | Comments                                                                                                                                                                                                                                        |
+===================+=================================================================================================================+=================================================================================================================================================================================================================================================+
| Variable          | Select which variable should define the groups (Independent or Dependent) from the dropdown menu.               | If the *independent variable* defines the groups, boxes will be plotted horizontally. If the *dependent variable* defines the groups, boxes will be plotted vertically                                                                          |
+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Variable Type     | Select whether the variable you have defined above is continuous or categorical from the dropdown menu.         | A continuous variable can be turned into a categorical variable when you use the binning feature.                                                                                                                                               |
+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Number of Bins    | Type the number of bins you would like data to be organized in.                                                 | This step may require trial and error based on how you wish to display data.                                                                                                                                                                    |
+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Bin Assignments   | Select how you would like data to be binned from the dropdown menu.                                             | -  **Evenly Distribute Population:** assigns bins based on the underlying data. For example, if the majority of the subjects in the study were elderly, bins based on age could look like: [(1-40), (40-80), (81-85), (86-90), (90-92)].        |
|                   |                                                                                                                 |                                                                                                                                                                                                                                                 |
|                   | **Note:** This feature can only be used when the variable type selected above is continuous.                    | -  **Evenly Spaced Bins:** creates bins based on the overall range of the variable. For example, if the majority of the subjects in the study were elderly, bins based on age could look like: [(1-20), (21-40), (41-60), (61-80), (81-100)].   |
+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Manual Binning    | Select the checkbox if you wish to bin manually.                                                                | Complete the binning form that populates as a result of checking the **Manual Binning** box.                                                                                                                                                    |
|                   |                                                                                                                 |                                                                                                                                                                                                                                                 |
|                   | **Note:** This is the only binning method available if you are attempting to bin a categorical variable type.   | For continuous data:                                                                                                                                                                                                                            |
|                   |                                                                                                                 |                                                                                                                                                                                                                                                 |
|                   |                                                                                                                 | |image163|                                                                                                                                                                                                                                      |
|                   |                                                                                                                 |                                                                                                                                                                                                                                                 |
|                   |                                                                                                                 | For categorical data:                                                                                                                                                                                                                           |
|                   |                                                                                                                 |                                                                                                                                                                                                                                                 |
|                   |                                                                                                                 | |image164|                                                                                                                                                                                                                                      |
+-------------------+-----------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
#. Click **Run**.

Data Binning Using Survival Analysis
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Data binning is used in survival analyses if the variable you wish to
use is continuous (for example, age), but needs to be viewed as
categorical data. Alternatively, it can be used to regroup categorical
data. For example, if histological grade with values such as *Well
Defined*, *Moderately Well Defined*, and *Poorly Defined* are selected,
you can group *Moderately Well Defined* with *Poorly Defined* and treat
them as one group for the purposes of this analysis.

#. To use the data binning feature with a survival analysis:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. Define the cohorts you wish to analyze by dragging one or more
      concepts from a study into empty subset definition boxes. For more
      information, see *Populating the Study Groups* .
#. Click the **Advanced Workflow** tab:

      |image165|
#. Select **Survival Analysis** from the **Analysis** dropdown menu:

      |image166|

      The Variable Selection section appears.
#. Define the variables:

+----------------------+-------------+---------------------------------------------------------------------------------------------------------+---------------------+
| Variable             | Required?   | Description                                                                                             | Example             |
+======================+=============+=========================================================================================================+=====================+
| Time                 | Yes         | A time variable used in the study.                                                                      | Survival Time       |
+----------------------+-------------+---------------------------------------------------------------------------------------------------------+---------------------+
| Category             | No          | A variable that you wish to use to sort the cohorts.                                                    | Cancer Stage        |
|                      |             |                                                                                                         |                     |
|                      |             | If the variable you wish to use is continuous (for example, age), the binning feature should be used.   |                     |
+----------------------+-------------+---------------------------------------------------------------------------------------------------------+---------------------+
| Censoring Variable   | No          | A censoring variable (occurs when the value of a measurement/observation is partially known).           | Survival (Censor)   |
+----------------------+-------------+---------------------------------------------------------------------------------------------------------+---------------------+
#. Under **Binning**, click **Enable**:

   |image167|
#. Define the following:

+-------------------+-----------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Field             | Description                                                                                                     | Comments                                                                                                                                                       |
+===================+=================================================================================================================+================================================================================================================================================================+
| Variable Type     | Select whether the variable you have defined above is continuous or categorical.                                | A continuous variable can be treated as a categorical variable when you use the binning feature.                                                               |
+-------------------+-----------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Number of Bins    | Type the number of bins you would like data to be organized in.                                                 | This step may require trial and error based on how you wish to display data.                                                                                   |
+-------------------+-----------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Bin Assignments   | Select how you would like data to be binned.                                                                    | -  Evenly Distribute Population: assigns bins based on the underlying data.                                                                                    |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   | **Note:** This feature can only be used when the variable type selected above is continuous.                    |    For example, if the majority of the subjects in the study were elderly, bins based on age could look like: [(1-40), (40-80), (81-85), (86-90), (90-92)].    |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   |                                                                                                                 | -  Evenly Spaced Bins: creates bins based on the overall range of the variable.                                                                                |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   |                                                                                                                 |    For example, if the majority of the subjects in the study were elderly, bins based on age could look like: [(1-20), (21-40), (41-60), (61-80), (81-100)].   |
+-------------------+-----------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Manual Binning    | Select the checkbox if you wish to bin manually.                                                                | Complete the binning form that populates as a result of checking the **Manual Binning** box.                                                                   |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   | **Note:** This is the only binning method available if you are attempting to bin a categorical variable type.   | -  For continuous data:                                                                                                                                        |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   |                                                                                                                 | |image168|                                                                                                                                                     |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   |                                                                                                                 | -  For categorical data:                                                                                                                                       |
|                   |                                                                                                                 |                                                                                                                                                                |
|                   |                                                                                                                 | |image169|                                                                                                                                                     |
+-------------------+-----------------------------------------------------------------------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------+
#. Click **Run**.

High Dimensional Data
~~~~~~~~~~~~~~~~~~~~~

The High Dimensional Data button available within the Advanced Workflow
section of Dataset Explorer allows you to specify additional inputs for
selected variables. These inputs help filter specific information of
value (such as platforms, samples, or timepoints).


.. note:: The High Dimensional Data feature must be used when you perform an analysis using high dimensional data (such as SNP, gene expression, RBM, etc.) symbolized by the DNA icon (|image171|). Additionally, the High Dimensional Data feature cannot be used without high dimensional data.


#. To use the High Dimensional Data feature:
#. Click the tranSMART **Dataset Explorer** tab to display the
      Dataset Explorer window.
#. In the left pane of the Dataset Explorer window, click the
      **Navigate Terms** tab.

      The navigation tree appears, showing the categories of available
      studies:

      |image172|
#. Select the study of interest.
#. Drag the study of interest into a subset definition box in Subset
      1.
#. Click the **Advanced Workflow** tab above Subset 1:

      |image173|
#. Select the analysis you wish to perform, and define at least one
      variable using high dimensional data.
#. Click the **High Dimensional Data** button.

      The Compare Subsets-Pathway Selection dialog appears.
#. Define the following available filters:


.. note:: Dataset Explorer will attempt to pre-populate default values in the associated fields of the dialog based on the underlying data in the variable selection box.


+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Filter                  | Description                                                                                                                                                                                                                                        |
+=========================+====================================================================================================================================================================================================================================================+
| Platform                | The platform type (for example, SNP, mRNA, etc.) used to collect biomarker data in the study.                                                                                                                                                      |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| GPL Platform            | The specific name of the platform used in the study.                                                                                                                                                                                               |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Sample                  | The type of sample tested in the study.                                                                                                                                                                                                            |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Tissue Type             | The type of tissue tested in the study.                                                                                                                                                                                                            |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Timepoint               | The time period when the sample was taken.                                                                                                                                                                                                         |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Select a Gene/Pathway   | The gene, gene signature, or pathway of interest.                                                                                                                                                                                                  |
|                         |                                                                                                                                                                                                                                                    |
|                         | If you would like to run the analysis on the entire chip, leave this field blank.                                                                                                                                                                  |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Select SNP Type         | Select the type of SNP data being used:                                                                                                                                                                                                            |
|                         |                                                                                                                                                                                                                                                    |
|                         | -  Genotype – Use for categorical variables.                                                                                                                                                                                                       |
|                         |                                                                                                                                                                                                                                                    |
|                         | -  Copy Number – Use for continuous variables.                                                                                                                                                                                                     |
|                         |                                                                                                                                                                                                                                                    |
|                         | **Note:** This option is only available when you drag SNP data into the variable selection box.                                                                                                                                                    |
|                         |                                                                                                                                                                                                                                                    |
|                         | **Note:** Both Genotype and Copy Number data may not be available for all studies involving SNP data.                                                                                                                                              |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Aggregate Probes?       | The checkbox can be selected if the variable chosen is either gene expression data or SNP copy number data.                                                                                                                                        |
|                         |                                                                                                                                                                                                                                                    |
|                         | If the checkbox is selected, the algorithm WGCNA (weighted correlation network analysis) is employed. For genes that are comprised of multiple probes, WGCNA selects the probe that best represents the overall expression level or copy number.   |
|                         |                                                                                                                                                                                                                                                    |
|                         | **Note:** WGCNA was developed by the Department of Human Genetics at UCLA. For more information, see http://www.genetics.ucla.edu/labs/horvath/CoexpressionNetwork/.                                                                               |
+-------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
#. Click **Apply Selections**.
#. Define any additional required variables, then click **Run**.

Other Features
~~~~~~~~~~~~~~

The sections below illustrate additional features in the Advanced
Workflow tab.

Save to PDF
^^^^^^^^^^^

The Save to PDF feature allows you to save analyses run through the
Advanced Workflow function within Dataset Explorer.

#. To save advanced workflow analyses as a PDF file:
#. Click the tranSMART **Dataset Explorer** tab to display the
      Dataset Explorer window.
#. In the left pane of the Dataset Explorer window, click the
      **Navigate Terms** tab.

      The navigation tree appears, showing the categories of available
      studies:

      |image175|
#. Select the study of interest.
#. Drag the study of interest into a subset definition box in Subset
      1.
#. Click the **Advanced Workflow** tab above Subset 1:

      |image176|
#. Select the analysis you wish to perform, and define the variables
      accordingly.
#. Click **Run**.

      Your analysis appears below the variable selection panes.
#. Click **Save to PDF**:

      |image177|

      The following dialog appears:

      |image178|
#. Select **Open with** or **Save File**, then click **OK**.

Download Raw R Data
^^^^^^^^^^^^^^^^^^^

Analyses run through the Advanced Workflow tool within Dataset Explorer
use R for computation. You are able to download raw R data for use in an
external tool.


.. note:: For more information on The R Project for Statistical Computing, visit the following site: *www.r-project.org*.


#. To download advanced workflow analyses as raw R data:
#. Click the tranSMART **Dataset Explorer** tab to display the
      Dataset Explorer window.
#. In the left pane of the Dataset Explorer window, click the
      **Navigate Terms** tab.

      The navigation tree appears, showing the categories of available
      studies:

      |image180|
#. Select the study of interest.
#. Drag the study of interest into a subset definition box in Subset
      1.
#. Click the **Advanced Workflow** tab above Subset 1:

      |image181|
#. Select the analysis you wish to perform, and define the variables
      accordingly.
#. Click **Run**.

      Your analysis appears below the variable selection panes.
#. Click **Download raw R data**:

      |image182|

      The following dialog appears:

      |image183|
#. Select whether you would like to open the file or save it to your
      hard drive, then click **OK**.

The Jobs Tab
------------

The Jobs tab allows you to review analyses you have run previously.

|image184|

Each advanced workflow analysis that you have run in the past seven days
is logged in the Jobs tab in a spreadsheet format.

The columns of information in the Jobs tab are described below:

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Column       | Description                                                                                                                                                  |
+==============+==============================================================================================================================================================+
| Name         | The name of the analysis run. The format of the name is as follows:                                                                                          |
|              |                                                                                                                                                              |
|              | |image185|                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Status       | The status of the analysis. Statuses are explained below:                                                                                                    |
|              |                                                                                                                                                              |
|              | -  **Completed** – The job has finished and a visualization or analysis is available.                                                                        |
|              |                                                                                                                                                              |
|              | -  **Started** – The job has been started and is still processing.                                                                                           |
|              |                                                                                                                                                              |
|              | -  **Uploading File** – You have selected to load additional data into your visualization, and the data is still in the process of uploading to tranSMART.   |
|              |                                                                                                                                                              |
|              | -  **Error** – The job did not complete due to an error.                                                                                                     |
|              |                                                                                                                                                              |
|              | -  **Cancelled** – The job was cancelled and will not complete.                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Run Time     | The time the analysis took to process.                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Started On   | The date and time that the analysis was started.                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


.. note:: Click the **Refresh** button to view any changes that have been made since the Jobs tab initially populated.


Viewing a Logged Job
~~~~~~~~~~~~~~~~~~~~~

Each advanced analysis that you have run in the previous seven days will
be logged in the **Jobs** tab. You may view the visualization or
analysis again by selecting it from the list.

#. To run a logged advanced workflow:
#. Run tranSMART, then click the **Dataset Explorer** tab.
#. In the right pane, click the **Jobs** tab:

      |image187|
#. Click the hyperlink of the analysis you are interested in viewing:

      |image188|
