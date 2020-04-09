+++
title = "User Manual"
date = 2020-04-03T12:34:36+13:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

![Koe works in most browsers, but has been tested most extensively in Chrome. If you experience issues, try Chrome first, then contact us.](https://i.ibb.co/7rp86F3/Koe-works-with-Chrome-only-3.png)

![To report bugs or suggest features, chat with us directly at facebook.com/KoeSoftware](https://i.ibb.co/XL9TCdw/Contact-us-Koe2.png)

![](https://i.ibb.co/SXpGd0r/Cite-us-Koe.png)


![Koe Bioacoustics Software](https://i.ibb.co/s608SrX/Koe-Logo-In-Circle-with-Word-next-to-it-SMALLER4.png)

***Koe*** **is open-source web-based software for analysing animal vocalisations.**

Read the  *Methods in Ecology and Evolution* paper [here](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/2041-210X.13336). **Please cite this paper if you publish using *Koe***


It features tools for visualising, segmenting, measuring, classifying, data-filtering and exporting acoustic units, and analysing sequence structure (syntax). It is an end-to-end acoustic database solution, especially suitable for animal species with distinct acoustic units.

You can use it on any device at [koe.io.ac.nz](https://koe.io.ac.nz), which makes it ideal for collaboration, education, and citizen science. 

For a quick overview and demonstration of program features, see this video:

{{< youtube 0RaLAJim_PA >}}

***Click [here](https://drive.google.com/open?id=1fEyWtzjim-32KNtisl1cXWcilCgxdHLR) to download NZ bellbird song recordings to follow along with the user manual*** 


Table of Contents
=================
- [Why use _Koe_?](#why-use-koe)
- [Overview of _Koe_ workflow](#overview-of-koe-workflow)
- [Navigating _Koe_](#navigating-koe)
- [Create an account](#create-an-account)
- [Create a new database](#create-a-new-database)
- [Add collaborators to a database and set permission levels](#add-collaborators-to-a-database-and-set-permission-levels)
- [Set database restore points](#set-database-restore-points)
- [Upload songs](#upload-songs)
- [Upload raw recordings and divide into songs](#upload-raw-recordings-and-divide-into-songs)
- [Recordings too big to upload? Use this tool to automatically split your wav files](#recordings-too-big-to-upload-use-this-tool-to-automatically-split-your-wav-files)
- [Segment songs into units, or...](#segment-songs-into-units)
- [Alternatively, import unit segmentation from csv](#import-unit-segmentation-from-csv)
- [Extract unit features](#extract-unit-features)
- [Construct ordination](#construct-ordination)
- [View interactive ordination and classify units](#view-interactive-ordination-and-classify-units)
- [Calculate similarity](#calculate-similarity)
- [View interactive unit table and classify units](#view-interactive-unit-table-and-classify-units)
  * [Sorting by columns](#sorting-by-columns)
  * [Classifying](#classifying)
- [Exemplars](#exemplars)
- [Filtering data](#filtering-data)
- [View all songs](#view-all-songs)
- [Mine sequence structure](#mine-sequence-structure)
- [Visualise sequence structure as a network](#visualise-sequence-structure-as-a-network)
- [Exporting your data](#exporting-your-data)
- [Copy songs to another database](#copy-songs-to-another-database)
- [Make database subsets (collections)](#make-database-subsets-collections)
- [Keyboard shortcuts](#keyboard-shortcuts)
- [[Analysis Tutorial: Case Study of NZ bellbird song]]
- [[Frequently Asked Questions]]

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


# Why use _Koe_?
[Back to table of contents](#table-of-contents)

Acoustic communication is fundamental to the behaviour of many species. If we want to understand animal behaviour we need tools that allow us to objectively examine the details of vocalisations. What information are they sharing, and how is it encoded?

Often, acoustic communication is structured as a temporal sequence of distinct acoustic units (e.g. syllables), where information is encoded in the _types_ of units and sometimes their _temporal arrangement_ (syntax). In such cases, this is the flowchart for acoustic analysis:

![Bioacoustics process](https://i.ibb.co/YXmS36F/bioacoustic-process-pp.png)

Classification is a key step, because once you have a dataset of labelled units, you can analyse repertoire size and sequence structure and compare between individuals, sexes, sites, and seasons.

Manual classification by human eye and ear remains the primary and most reliable method for most species, but is hindered by a lack of tools, especially for large and diverse datasets.

That’s where _Koe_ comes in. By facilitating large-scale, high-resolution classification and analysis of acoustic units, _Koe_ opens up many possibilities for bioacoustics research.

# Overview of _Koe_ workflow
[Back to table of contents](#table-of-contents)

We designed the _Koe_  workflow to be intuitive and flexible. Here is a suggested workflow:
 
![_Koe_ workflow](https://i.ibb.co/w4tNkZ5/workflow-SMALL.png)

* **Import** raw recordings and divide into “songs” (vocalisation bouts), then **segment songs** into their constituent acoustic units. 

* You can **extract acoustic features** from units. These features are used to calculate unit similarity and expedite classification in two ways: through interactive ordination, and similarity indices.

* **Interactive ordination** is a major time saver for classification. The user can encircle groups of points on the ordination to see spectrograms, hear playback, and bulk-label groups of units. Harnessing the interactive ordination in conjunction with human audio-visual perception, this technique offers a major advance in both speed and robustness over existing acoustic classification methods.

* Units can also be viewed as an **interactive unit table**. A key feature of the unit table is the **similarity index**, which lets you sort by acoustic similarity. Because similar-sounding units are grouped together, units can easily be selected in bulk and classified.

* A **catalogue of class exemplars** is generated automatically, displaying up to 10 randomly chosen exemplars for each class, which serves as a useful reference during classification.

* _Koe_ gives you full control of your databases, allowing you to **add collaborators** and set permission levels. This makes it straightforward to conduct a classification validation experiment: grant judges labelling access to your database, and once they have independently classified the units, compile their labels to examine concordance.

* Once units have been classified, songs can be visualised as sequences of unit labels; you can filter by sequence to identify all instances of a specific song type, for example. You can also **mine sequence structure** in detail with association rule algorithms and network visualisations.

* **Export data** from any program view as csv.

# Navigating _Koe_
[Back to table of contents](#table-of-contents)

In _Koe_, on the left of the screen is a sidebar with program controls. At the top of the sidebar are User account controls for logging out / switching user; beneath that are controls specific to the active view. And beneath that is the workflow navigation pane with buttons to access different program views, labelled according to their function. 
 
![Sidebar](https://i.ibb.co/gdV4Pjc/Side-Bar-SMALLER.png)

# Create an account
[Back to table of contents](#table-of-contents)

Go to [koe.io.ac.nz](https://koe.io.ac.nz) and click on **Register** to register an account. 

Choose a username, input your name and email address for purposes of _Koe_ support correspondence, and choose a password. (We will never share your information with anyone).
  
![](https://i.ibb.co/xD1nLZ1/Sign-Up-Code-Removed.png)


# Create a new database
[Back to table of contents](#table-of-contents)

Under Manage your database, click **New database** to create a new database.
 

![](https://i.ibb.co/0fSKJj6/Manage-Database.png)

# Add collaborators to a database and set permission levels
[Back to table of contents](#table-of-contents)

You can add collaborators at any stage. 

1. Click on _Manage your database_.

2.  Select the round checkbox of the database you want to add collaborators to.

3. Click **Add collaborator** and Type the _Koe_ username or _Koe_ account email address of your intended collaborator. 

4. Once added, you can set their permission level by double-clicking the **Permission** cell next to their username. 

![](https://i.ibb.co/drg4pMf/Manage-Database-Add-Collaborators.png)


From lowest to highest permission level: View, Annotate, Import data, Copy files, Add files, Modify segmentation, Delete files, Assign user. Each subsequent permission level extends the permissions of the previous level as per the table below:

Level|Permissions
---|---
View|User can view data
Annotate|User can view and annotate data
Import data|User can import, view and annotate data
Copy files|User can copy files, import, view and annotate data
Add files|User can add files, copy files, import, view and annotate data
Modify segmentation|User can modify segmentation, add files, copy files, import, view and annotate data
Delete files|User can delete files, modify segmentation, add files, copy files, import, view and annotate data
Assign user|User can assign additional users, delete files, modify segmentation, add files, copy files, import, view and annotate data


# Set database restore points
[Back to table of contents](#table-of-contents)

Changes are saved to the database as soon as they happen. If you want to be able to revert to a previous state you will want to save database restore points. 

1. Click on _Manage your database_.

2. Select the round checkbox of the database you want to set a restore point for.

3. Click **Quick save** or **Full save** at the bottom of the window to create a restore point. **Quick save** saves label data associated with each unit. **Full save** saves both label data and segmentation start/end points.

***Please note*** that restore points do not affect which songs are in the database or which units are segmented. For example, if you make a save and then delete songs, reverting will not restore the songs to the database. Similarly, if you add songs, reverting will not remove the added songs. In the same way, if you add/delete units, reverting will not remove/restore the segmentation. What reverting _will_ do is restore the label data and (for a full save) the segmentation start/end points for *currently existing* units. If you want to preserve all aspects of a database at a certain point, like a traditional 'Save As', then copy everything to a new database, as described in [Copy songs to another database](#copy-songs-to-another-database) below.  


# Upload songs
[Back to table of contents](#table-of-contents)

[*Click this link to download NZ bellbird songs to try out **Upload songs** feature and subsequent steps*](https://drive.google.com/open?id=1fEyWtzjim-32KNtisl1cXWcilCgxdHLR)

If you have already-divided song files on your computer, you can upload these directly. On the navigation pane, click **Upload songs** and select up to 100 WAV files at once to upload. 

 ![](https://i.ibb.co/t8hLv6c/Upload-Songs.png)

For raw recordings that need to be divided into songs, see next step.

# Upload raw recordings and divide into songs
[Back to table of contents](#table-of-contents)

[*Click this link to download raw (unsplit) recordings of bellbird song to try **Upload & split raw recordings***](InsertLinkToRaw)

To upload a raw recording and divide it into song selections, do the following: 

On the navigation pane, click *Upload & split raw recording*

1. In the **Upload raw recording** dialogue box, Click **Upload (WAV only)**

2. Select the recording you want to upload

3. Click **Open**

![](https://i.ibb.co/m67XVZS/Upload-Raw1.png)

After selecting a file to upload, an **Upload raw recording** dialogue appears with **Track name** and **Record date** fields. The track name is automatically filled in based on the `wav` filename. For example, `Raw_Recording_001.wav` will by default appear as `Raw_Recording_001`. 

4. Click in the **Track name** field to modify the track name, if you wish. 

5. Click in the **Record date** field to modify the date. By default, the record date is set as the date of recording upload to _Koe_. 

6. Click **Submit track info**.


![](https://i.ibb.co/sW1HrHS/Upload-Raw-Recording-Date-Screen.png)

7. For recordings with more than one channel, select the desired channel. 

8. Play the recording with the playback controls, looking for songs to segment. To play from the beginning, click **Play** button. 

9. You can also play from a specific timepoint by clicking that point, then clicking **Play**. 

With the controls beneath the spectrogram, you can:

10. Adjust spectrogram zoom.

11. Adjust spectrogram colour map. 

12. Adjust playback speed.

13. Adjust spectrogram contrast.

 
![](https://i.ibb.co/TbM0kvF/Split-Raw-Ver2.png)

14. To create a song selection simply drag over the spectrogram to create a selection box. 

![](https://i.ibb.co/zZv1WcG/Click-and-Drag-song-sel.png)

Click the selection box to play it. Adjust the selection box endpoints by holding `Shift` and dragging the box handles that appear.
 
For each selection you make, a row appears in the table beneath. 

15. Fill in annotation columns as desired by double-clicking in those cells.  
 
![](https://i.ibb.co/tbsN2zP/Naming-Scheme-And-Annot.png)

16. You can set an automatic naming scheme for segmented songs. Click the **Naming pattern** box to create a naming scheme with any combination of the following components: `Track name`, `Year`, `Month`, `Day`, `Order`. You can also add custom components to the scheme, such as text strings, if you wish. Click **Rename all** to apply the naming scheme to all existing song selections.

17. Once you’ve finished making song selections, click **Save** to upload the songs to the database. The raw recording will not be saved, only songs – so make sure you finish partitioning all songs in one go.

# Recordings too big to upload? Use this tool to automatically split your wav files
Some bioacoustics researchers work with looong recordings (e.g. passive acoustic monitoring). Very large files can be cumbersome. But don't worry! Yukio Fukuzawa has heard your cries and has come galloping to our rescue with a simple tool for automatically splitting large wav files into smaller wav files. You specify how long you want the audio sections to be, and how many seconds of overlap between sections. 

To run the tool you will need to install Python. After that it's just a simple line of code that you type into your command prompt.

The tool and instructions are found here: [https://github.com/fzyukio/split-songs](https://github.com/fzyukio/split-songs)

# Segment songs into units
[Back to table of contents](#table-of-contents)

This section describes how to segment songs into acoustic units. However, if you have already segmented units using other software, jump to the [next section](#import-unit-segmentation-from-csv)

On the navigation pane, click *View all songs*. You will see your list of songs; click on a song filename to open the song. 
 
![](https://i.ibb.co/fvvjKJ5/Click-a-filename.png)

Much like the previous program view, you can play the song and adjust spectrogram appearance and playback speed. Drag over units on the spectrogram to segment. Mouse over a selection box to highlight that unit’s row in the table. Click a selection box for playback. Fill in annotation columns as desired. Then click **Save segmentation** to save to the database.

***You can return to this view to alter segmentation at any time***.

***Note: a _Koe_ user interested in comparing entire songs as units for analysis can still use the software by selecting songs rather than syllables as units and classifying them using interactive ordination / unit tables. In a future update, we hope to offer both unit- and song-level comparisons simultaneously, so that a user does not have to choose.*** 
 
![](https://i.ibb.co/X7S5V6G/Segmentation-view.png)

# Import unit segmentation from csv
[Back to table of contents](#table-of-contents)

If you have already segmented units using other software, you can import the unit segmentation start/end point data into Koe, and avoid doing it over again in Koe. You're welcome!
1. Upload all the song wav files that you have start/end-point data for (see [Upload songs](#upload-songs))

2. Navigate to *Classify and manage units > Unit table* on the left-hand pane. 

3. Click the **Export current table as csv** button. 

4. Open the resulting csv file (in *Excel*, for example).

5. Leaving the column headers unchanged, input your desired filename and unit start/end time information into the table, with one row per unit. 

(Note that start/end times are measured in ms from the start of the file. E.g. a unit with *start* column value of 680 and *end* column value of 750 means the unit begins 680 ms and ends at 750 ms from the start of the file. Koe will use this information to construct syllable boundaries.)

6. *Excel* may have reformatted values in the date column. You need to make sure the date format is yyyy-mm-dd. 

7. Save the updated csv file. 

8. In *Koe*, go to *Classify and manage units > Unit table*, and click **Import data (csv) to table**. Browse to select your csv file.

Your data should appear, and if everything worked properly you will see spectrograms of segmented units.

# Extract unit features
[Back to table of contents](#table-of-contents)

You can extract a wide array of acoustic features from units. These features are used to calculate unit similarity, which is used for constructing ordination and calculating similarity indices. You can also export extracted features as a data matrix (`csv` file).

Go to *Extract features and compare* > *Extract unit features*, then:

1. Select the desired set of features (if in doubt, tick all of them to start with).

2. Select the desired set of aggregation methods (see below for explanation).

3. Type a name for the data matrix (e.g. “All features”). 

4. Click **Submit**. 

 ![](https://i.ibb.co/TczFB5s/Choosing-Feature-Set3.png)

The _Koe_ server will process your request and send a notification email when your extraction job finishes. (Typically this will take only a minute or two). You can see what sets of features you have previously extracted under the Existing data matrices dropdown in this view.

Here are the features offered, with descriptions of each (*coming soon*): 

Feature | Description
--- | ---
spectral flatness|
spectral bandwidth|
spectral centroid|
spectral contrast|
tonnetz|
spectral rolloff|
chroma stft|
chroma cqt|
chroma cens|
mfcc|
zero crossing rate|
total energy|
aggregate entropy|
average entropy|
average power|
max power|
max frequency|
frequency modulation|
amplitude modulation|
goodness of pitch|
amplitude|
normalise|
entropy|
mean frequency|
spectral continuity|
duration|
frame entropy|
average frame power|
max frame power|
dominant frequency|	

Most of these features are frame-based, with the result that units of different lengths are represented by unequal-length feature sequences. It is therefore necessary to aggregate these sequences to arrive at the same dimensional representation for each unit, so that units can be compared.
Aggregation methods offered:

Aggregation method | Description
--- | ---
Mean|
Median|
Standard Deviation|
Divcon_3_mean|
Divcon_5_mean|
Divcon_7_mean|	

To export extracted feature matrices as `csv` for external use, click **Download**. 

***If your dataset is very big, you will need a lot of free RAM for this to work. For example, with 21k units, you will need at least 8 GB of free RAM***.

# Construct ordination
[Back to table of contents](#table-of-contents)

_Koe_ can produce interactive two- or three-dimensional ordination plots, based on the unit features extracted in the previous step. Notably, two-dimensional plots can be used to classify units directly on the plot, which greatly expedites the classification process (see next section). To construct an ordination, go to **Extract features and compare > Construct ordination** and choose a data matrix from the Existing data matrices dropdown list (1). 

![](https://i.ibb.co/9yYhTSD/Construct-Ordination3.png)

Choose an ordination method (2): **PCA** (Principal Components Analysis), **ICA** (Independent Component Analysis) or **t-SNE** (t-distributed Stochastic Neighbor Embedding) with PCA prepocessing. Since t-SNE preserves local structure in the data, it is particularly effective for defining and discriminating between different clusters. 

*Note*: t-SNE is controlled by two parameters, 'perplexity', which can be set to any value between 5 and 50, and number of iterations. By default, perplexity is set to 10 and number of iterations (n_iter) is set to 4000. There is no 'correct' value of perplexity -- you must experiment with different values to achieve best results. If the perplexity value you choose is too high or low, you will find points on the plot do not cluster well by similarity, and will form convoluted banding patterns. To change the value, type, e.g. **perplexity=30** in the **Extra parameters** box. The numbers of iterations should be adequate in most cases at 4000, but you can change this  by typing, e.g. **n_iter=5000** in the **Extra parameters** box. To control both parameters, separate with a comma as in **perplexity=30, n_iter=5000**.

Choose (3) the desired number of dimensions: two or three. Then click **Submit** (4). The _Koe_ server will process your request and send a notification email when your ordination construction job finishes. (Typically this will take only a few minutes).

For more tips on optimising your t-SNE ordination in **Koe**, see [this FAQ](https://github.com/fzyukio/koe/wiki/Frequently-Asked-Questions#how-do-i-get-my-tsne-ordination-to-cluster-nicely) 

# View interactive ordination and classify units
[Back to table of contents](#table-of-contents)

Click **Classify & manage units > Ordination**. If you have constructed several ordinations, choose the one you want from the Current ordination dropdown list in the active view controls on the side bar.
For 2D ordinations, a plot will be generated like the below. 

![](https://i.ibb.co/JRNBgGf/Ordination-view-small.png)

The plot is controlled by a toolbar at the top left of the plot:

 
![](https://i.ibb.co/Kh7MqC6/Plot-buttons.png)

With the lasso tool (selected by default), encircle groups of points on the plot to see their spectrograms. Mousing over a point in a selection highlights the corresponding spectrogram in the left-hand panel. Click a point on the plot or its spectrogram for audio.

Classify selections in bulk by clicking **Label** beneath the spectrograms pane. You can label at up to three levels of granularity. 
 

![](https://i.ibb.co/QXn4y1b/Label-button-in-ordination-view.png)


As you add more classes, they each acquire a distinctive point type. Toggle class visibility by clicking the legend, zoom the plot (with the zoom tool) for more refined detail.

You can also view selections as an interactive unit table by clicking **View table**. More information on the unit table below.

# Calculate similarity
[Back to table of contents](#table-of-contents)

A second method for expediting classification is to use unit similarity indices. In the unit table (below) the similarity index is used to sort your units by spectral similarity, assisting rapid manual classification by grouping syllables in clusters that can be labelled in bulk.

You have two input options for calculating a similarity index: one is to use an extracted feature set, and the other is to use the coordinates of a constructed ordination. Go to **Extract features and compare > Calculate similarity** and select an option from Existing data matrices (for the former option) or Existing ordinations (for the latter).  For optimal results we recommend using an existing t-SNE ordination as the input for the similarity index. Then click **Submit**. The _Koe_ server will process your request and send a notification email when your similarity calculation job finishes. (Typically this will take only a few minutes). 

# View interactive unit table and classify units
[Back to table of contents](#table-of-contents)

Click on **Classify & manage units > Unit table** to see all your units as an interactive unit table. 

 
![](https://i.ibb.co/wWpzWN6/Unit-Table-1.png)

Much like in *Excel*, you can click on a cell to select it, or move around the grid with the arrow keys. `Page Up` and `Page Down` will page through one screen-height at a time. To hear a syllable, simply click on its spectrogram, or press `spacebar` with spectrogram cell selected. There is a speed slider at the top of the sidebar for slowing down playback; this helps our human ears hear details not apparent at full speed. Single-click on a cell to select cell contents (e.g. to copy to the clipboard), or double-click on a cell to alter cell content, if it is editable (editable cells contain a pencil icon).

Unit table columns (re-order columns simply by dragging their headers):

Column name|Description
---|---
ID|Unique syllable ID
Start|Start time of the syllable (milliseconds from song start).
End|End time of the syllable (milliseconds from song start).
Duration|Duration of the syllable (in milliseconds)
Individual|The ID of the vocalising individual
Song|Name of the song file the syllable comes from
Checkbox|This is the column you will use for selecting rows.
Spectrogram|Shows a spectrogram of the raw signal. Click to hear audio.
Label columns (Label, Subfamily, Family)|These are where you label your units. There are three independent columns for different levels of label granularity. Label is for the most fine-scale labelling, Subfamily is broader, and Family is the broadest.
Sex|The sex of the vocalising individual
Quality|The quality of the song. For example, you could use EX = Excellent, VG = Very Good, G = Good, OK = Ok, B = Bad.
Similarity Index|Sort by this column to group syllables by acoustic similarity (provided you have calculated similarity index as above).
Note|Write notes about a row (free format)
Date|The date of the raw recording
Added|The date the song was added to the database

If you change 'sex' or 'species' column info associated with an individual animal, the changes will be reflected for all rows in the table belonging to that individual (you may need to refresh your browser to see the change propagate). This prevents mistakes, such as the same individual being ascribed male sex in some rows and female sex in other rows. It also means you only have to enter sex and species information for an individual in one row.

A future _Koe_ update will allow a user to add custom annotation columns, such as a species column. In the meantime a user can simply co-opt one of the existing annotation columns for their purposes, such as labelling species. 

## Sorting by columns
[Back to table of contents](#table-of-contents)

Sort by a column by clicking on its header (e.g. **Duration**). To sort by multiple columns at once, `Shift+click` subsequent headers.

## Classifying
[Back to table of contents](#table-of-contents)

Units can have three sets of labels at once, using the three label columns: Label, Subfamily and Family. You can use these to label at different scales, e.g. fine-scale, intermediate-scale and broad-scale classification. Or you may choose to use these columns for other purposes.  

Select multiple rows of the same type by clicking their checkboxes or pressing spacebar with the checkbox cell selected. When you have finished selecting rows, press `Ctrl+Shift+L` to bulk label all selected rows at the fine-scale level. `Ctrl+Shift+F` bulk labels at the broad-scale “Family” level, and `Ctrl+Shift+S` bulk labels at the intermediate “Subfamily” level. 

Alternatively, click the menu button on the right-hand side of the **Label**, **Subfamily** or **Family** column header and select **Bulk set value**:

![](https://i.ibb.co/X4Mb8SV/Set-Label2.png)
A dialogue box will appear:

![](https://i.ibb.co/6rRVYxX/SetLabel.png)

If you are creating a new class, type any new name you like. If you are adding a group of units to a pre-existing class, then start typing the name of the class and it will appear in the dropdown list. The numbers beside each label class in the dropdown list indicate how many instances of that class there are in the dataset. Click the correct class name on the list, then click Set. All selected rows will now have this label.

Note that after labelling, all selected rows will remain selected. You can un-select all rows quickly with `Ctrl`+`

You can also classify an individual unit by double-clicking the label, subfamily or family cell and typing a string. If the label class already exists you will see it in the dropdown list. Click the list item you want, or use `Alt+Down` to navigate down the list and `Enter` to select:

![](https://i.ibb.co/1LGTDdZ/Double-click-cell-to-name.png)

# Exemplars
[Back to table of contents](#table-of-contents)

Every new label class you create gets automatically added to the **Exemplars** view, which functions as a class catalogue to reference during classification. This view has one row per type, with up to 10 randomly-selected exemplars for each row. Go to **Classify & manage units > Exemplars** to see your exemplars. Click on spectrograms to play the sound, and change playback speed with the speed slider, just as in other views. Click **Next 10 random exemplars** to randomly select the next batch. 
 
![](https://i.ibb.co/gTPWXNQ/exemplars-3.png)

You can have _Koe_ open in as many tabs or windows as you want, so it’s easy to have exemplars in one tab and unit table in another, to help you label by comparison. If you make changes in one tab, refresh your other tabs to see the changes.

# Filtering data
[Back to table of contents](#table-of-contents)

The filter box at the top of each program view is a quick and powerful way to filter your data. It takes regular expressions (see https://www.computerhope.com/jargon/r/regex.htm for a crash course on using regex), but it can also be used simply with no technical expertise. Simply mouse over a column header, click the dropdown arrow that appears, and select **Filter**. 

![](https://i.ibb.co/mhG32KG/Using-the-filter.png)

Then type the string you want to filter by. For example, in the unit table, to filter rows with a certain label, click the **Label** column dropdown and click **Filter**, then type a string, e.g.

`label: crazysqueak`

You can also filter by multiple columns at once, separated by semicolons.
`label: crazysqueak; song: BobtheBat_1`

To filter date columns (i.e. **Date of record** and **Added** columns), use the format `from(yyyy-mm-dd)to(yyyy-mm-dd)`, like this: `date: from(2015-01-01)to(2018-12-31)` 

To filter numerical columns, such as ID, use `==` for 'exactly', `>` and `<` for 'greater than' and 'less than', respectively. 

`^` indicates the start of a string, and `$` indicates the end; for example, 
`label: squeak` 
will return rows with ‘squeak’ anywhere in the label, such as ‘crazysqueak’, ‘squeaky’, ‘upsqueak’.

`label: ^squeak`
will return rows beginning  with ‘squeak’, such as ‘squeaky’.

`label: squeak$`
will return rows ending  with ‘squeak’, such as ‘crazysqueak’, ‘upsqueak’.

`label: ^squeak$`
will return rows with exactly ‘squeak’ (nothing before or after).

`label: ^$`
is a handy way of finding rows with blank labels.

# View all songs
[Back to table of contents](#table-of-contents)

Click on **View all songs**. Here you can see all your songs, with one row per song. You will see the song sequence structure as a sequence of unit labels.

To illustrate, the figure below shows a song (upper panel) and how it is represented in **View all songs** as a string of labels (lower panel). 
 
![](https://i.ibb.co/DCp3vCg/Songs-view.png)
Click on a unit to play it and see its spectrogram:
  
![](https://i.ibb.co/QkDJnqk/Songs-view-click-on-unit.png)

Click the play button at the start of a sequence to play the entire song. Use the filter to search for songs of a particular unit sequence, e.g.
`sequence:"trill"-"dragon"`
will filter for all songs with a `trill` unit immediately followed by a `dragon` unit. This is useful for finding songs with a shared pattern and exploring syntax.

# Mine sequence structure
[Back to table of contents](#table-of-contents)

As one way of exploring rules that may govern song structure (i.e. syntax), _Koe_ uses the cSPADE (constrained Sequential Pattern Discovery using Equivalence classes) algorithm ([Zaki, 2001](https://link.springer.com/article/10.1023/A:1007652502315)) to discover commonly-occurring sequences in a set of songs.

We  consider a sequence to be an ordered list of acoustic units denoted as `A⇒B⇒C⇒...⇒x`. 

A sequence rule has two parts: a left side (what comes before) and a right side (what follows). The rule states that when the left side occurs, the right side follows 

`[Left side]`⇒`[Right side]`

For example, take `A⇒B` ⇒ `C`. 
This rule states that when the sequence `A⇒B` occurs, `C` comes next.  

The left side can be a sequence of any length, but in our current implementation the right side is always one unit long For example:

`A`⇒`B` 
(when `A` occurs, `B` comes next)

or 

`A⇒B⇒C⇒D⇒E⇒F⇒G⇒H⇒I`⇒`J`
(when `A⇒B⇒C⇒D⇒E⇒F⇒G⇒H⇒I` occurs, `J` comes next).

We plan to relax this restriction in a future update to allow chains of units on the right side.
 
The cSPADE algorithm calculates the credibility of sequence rules. Credible rules have a large *confidence factor*, a large level of *support* and a value of *lift* greater than one (as defined below). Let's take the example rule `A⇒B` ⇒ `C`

**Support**: The level of support is the proportion of songs in the database that contain the entire sequence `A⇒B⇒C` at least once.

**Confidence**: The strength of an association is defined by its confidence factor (hereafter ‘confidence’), which is the proportion of those songs containing `A⇒B` that also contain `A⇒B⇒C`.

**Lift**: Lift is a measure of the strength of the association _relative to chance_. It is equal to the confidence of the rule, divided by the proportion of songs containing the right side. Thus it gives the *ratio* of (i) the proportion of songs the transition from  `A⇒B`⇒`C` occurs in, *versus* (ii) the proportion of songs expected to contain `A⇒B`⇒`C` by chance association. 

Think of our example rule, `A⇒B`⇒`C`. Imagine a dataset with 100 songs, where 10 of those songs contain `A⇒B`, 7 contain `A⇒B⇒C`, and 20 songs contain `C`. 

The *support* is **0.07** (i.e. `A⇒B⇒C` occurs in 7/100 songs). The *confidence* is **0.7** (i.e . `A⇒B⇒C` occurs in 7/10 songs containing `A⇒B`). The *lift* is the confidence (0.7) divided by the proportion of songs containing `C` (0.2), which is **3.5**. In other words, the association `A⇒B`⇒`C` occurs in 3.5 times as many songs as expected by chance association of `A⇒B` and `C`.

To demonstrate cSPADE with real data, consider the ten songs shown in the figure below to be a population of songs.  

![](https://i.ibb.co/5xJ6y8C/Half-of-Song-View.png)
 
The rule 

`Stutter⇒Waah(magpie)` ⇒ `Pipe(B6)`

has a *support* of 0.4 since the entire sequence occurs in four of the 10 songs. The rule has a *confidence* of 0.8, because in four of the five songs that contain `Stutter⇒Waah(magpie)`, the transition to `Pipe(B6)` occurs.  The proportion of songs with `Pipe(B6)` is 0.6, so the *lift* of this rule is 0.8/0.6=1.33. That is, the association `Stutter⇒Waah(magpie)` ⇒ `Pipe(B6)` occurs in 1.33 times as many songs as expected by chance association of `Stutter⇒Waah(magpie)` and `Pipe(B6)`.

# Visualise sequence structure as a network
[Back to table of contents](#table-of-contents)

![](https://i.ibb.co/QpyGwQj/c-SPADEand-Network-1.png)

Two-unit associations from cSPADE can be visualised using a directed network. The network models the direction and strength of association between pairs of units, across a population of songs. Units are represented by nodes (vertices) which are joined by lines (edges) if the units occur consecutively (by default _Koe_ shows only those sequences that occur in at least 1% of songs).  The order of units is indicated by arrow direction, and strength of association between units (lift) is represented by edge thickness. Visually cluttered networks can be simplified using the filter, e.g. to show only associations with high lift.

Control network appearance with the following controls:

Network control | Description
--- | ---
Separate units by actual time (on/off)|Activate Max/Min gap controls
  *Max gap* (10ms-1000ms)|The maximum gap length between units before they are no longer considered to be in the same sequence
  *Min gap* (1ms-100ms)|The minimum gap length between units below which they are no longer considered to be in the same sequence
Show pseudo begin and end (on/off)| Displays start and end nodes, to visualise which classes tend to start and/or end songs 
Show node labels (on/off)| Toggle visibility of node labels
Reactive pseudo start (on/off)| Pulls starting units towards the start node
Reactive pseudo end (on/off)| Pulls ending units towards the end node
Centering (on/off)| Prevents the network clumping in a corner of the screen
Repulsion (1-50)| Determines the extent to which nodes actively repel each other
Distance (10%-400%)| Determines how ‘spread out’ the nodes are

Nodes can also be dragged around with the mouse to optimise network appearance.

# Exporting your data
[Back to table of contents](#table-of-contents)

You can export the data from each program view as a CSV file by clicking **Export entire table (csv)** or **Export filtered subset (csv)** on the active controls pane. The format of exported tables matches how the data appears in _Koe_; for example, data exported from the _Unit table_ view will match the column and row order of the unit table as it appears in _Koe_. 

# Copy songs to another database
[Back to table of contents](#table-of-contents)

First make sure you have created the database which you want to copy songs to. Then, under **View all songs**, select the songs you want to copy (1), and click **Copy to another database** (2). Type the name of the database to copy to (3) then click **Yes** (4)

![](https://i.ibb.co/Lz1Ltz2/Copy-Songs-to-new-database.png)

# Make database subsets (collections)
[Back to table of contents](#table-of-contents)

You can make collections of units as convenient subsets for analysis. Under **Classify & manage units > Unit table**, select all the units you want to be in the collection, then click **Make a Collection from selected units** on the active controls pane. Type a name for the collection, then click **Set**. Note the Collection name must be unique; if the collection name has already been created (by any users, not just you), the name will not 'take'. Also note that a Collection is not separate from the parent database – any changes you make to the Collection will be reflected in the parent database. Therefore you should take care when naming the collection so that you will remember which parent it belongs to. You can rename and delete collections under **Manage your database**.
 
If you want to create a subset that you can modify independently from the parent database, go to **View all songs** and copy songs to another database. Then you can edit freely without affecting the original database. To achieve this, do the following:

1. [Create a new database](#create-a-new-database) under _Manage your database_.

2. Go to _View all songs_.

3. Under the **Current database** dropdown list on the controls pane, choose the database you want to copy songs *from*.

4. Select the songs you want to copy by checking their checkboxes.

5. Click **Copy to another database** on the active controls pane.

6. Type the name of the newly created database you want to copy songs *to*.

7. Click **copy**


# Keyboard shortcuts

### Browser shortcuts
**In Chrome:**
|Hotkey|Action|
|--|--|
|`Ctrl`+`Page Up` / `Ctrl`+`Page Down`|Toggle between browser tabs|
|`Alt`+`D`, then `Alt`+`Enter`|Duplicate current tab|
|`F5`| Refresh current tab
|`F12` (brings up developer panel) + long-click browser refresh button > *Empty Cache and Hard Reload*|Can resolve _Koe_ glitches. Try it—if you don't mind emptying your cache 

### Navigating data tables generally
These hotkeys are common to all views with data tables. Additional view-specific hotkeys are given in the following sections.
|Hotkey|Action|
|--|--|
|`←` `↑` `↓` `→`|Navigate the table grid|
|`Home`|Jump to first cell in row
|`End`|Jump to end cell in row|
|`Page Up`/`Page Down`|Page the table one screen-height at a time|
|`click` on table header, `Shift`+`click` on subsequent headers|Sort by multiple columns, in the priority order headers were clicked|

### *View all songs* view
|Hotkey|Action|
|--|--|
|`Spacebar`|Check/uncheck checkbox when checkbox cell is active|
|`Shift`+`click` on checkbox| Select a range (i.e. selects all rows between the last selected checkbox and the `Shift`+clicked checkbox)|

### Segmenting songs into units—*Segment songs into units* view

|Hotkey|Action|
|--|--|
|`Shift` while mousing over segmented unit box|Reveal unit selection box start/end handles; click and drag handles while holding `Shift` to adjust|
|`Hotkey coming`/`Hotkey coming`|Page spectrogram one screen-width forwards/backwards, to navigate through a recording quickly while segmenting units|
|`Spacebar`|Check/uncheck checkbox when checkbox cell is active|
|`Shift`+`click` on checkbox| Select a range (i.e. selects all rows between the last selected checkbox and the `Shift`+clicked checkbox)|

### Classifying units—*Unit table* view
Units can have three sets of labels at once, using the three label columns: *Label*, *Subfamily* and *Family*. You can use these to label at different scales, e.g. fine-scale, intermediate-scale and broad-scale classification. Or you may choose to use these columns for other purposes—it's up to you!  

|Hotkey|Action|
|--|--|
|`Spacebar`|**Play audio** (when spectrogram cell is active); **Check/uncheck** row selection checkbox (when checkbox cell is active) |
|`Shift`+`click` on checkbox| Select a range (i.e. selects all rows between the last selected checkbox and the `Shift`+clicked checkbox)|
|`Ctrl`+`Shift`+`L`| bulk-label all selected rows in *Label* column (e.g. fine-scale classification) |
|`Ctrl`+`Shift`+`S`|bulk-label all selected rows in *Subfamily* column (e.g. intermediate-scale classification)|
|`Ctrl`+`Shift`+`F`|bulk-label all selected rows in *Family* column (e.g. broad-scale classification)
|`Ctrl`+ `Grave accent key` (same key as ~ but without shift) |**Deselect** all currently selected rows|


**Suggestions for other hotkeys? Let us know!**


=================================================

JUMP TO: [[Analysis Tutorial: Case Study of NZ bellbird song]].

JUMP TO: [[Frequently Asked Questions]]

JUMP TO: [[What's new in Koe?]]

----------------

{{% children depth=999 %}}