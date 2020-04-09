+++
title = "Analysis Tutorial: Case Study of NZ bellbird song"
date = 2020-04-03T12:34:36+13:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

![](https://i.ibb.co/ZNT7vyJ/Bellbirds-On-Stick.jpg)
**NZ bellbird (_Anthornis melanura_) male (front) and female (back)**.

Here we give a detailed walk-through tutorial of the analyses performed in Fukuzawa et al. (2020) [https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.13336](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.13336).

Table of Contents
======================
  * [Getting started](#getting-started)
  * [Trying out the filter](#trying-out-the-filter)
- [What is the overall unit diversity for male and female bellbirds across all seven sites?](#what-is-the-overall-unit-diversity-for-male-and-female-bellbirds-across-all-seven-sites-)
  * [Find the total number of classes](#find-the-total-number-of-classes)
  * [Make a database subset for males](#make-a-database-subset-for-males)
  * [Make a database subset for females](#make-a-database-subset-for-females)
  * [Find how many classes are sung by males](#find-how-many-classes-are-sung-by-males)
  * [Find how many classes are sung by females](#find-how-many-classes-are-sung-by-females)
  * [Calculating repertoire overlap](#calculating-repertoire-overlap)
- [How many male unit types are now shared between Tawharanui and source population Hauturu?](#how-many-male-unit-types-are-now-shared-between-tawharanui-and-source-population-hauturu-)
  * [Make a subset for males on LBI](#make-a-subset-for-males-on-lbi)
  * [Make a subset for males on TAW](#make-a-subset-for-males-on-taw)
  * [Find repertoire size for males on LBI](#find-repertoire-size-for-males-on-lbi)
  * [Find repertoire size for males on TAW](#find-repertoire-size-for-males-on-taw)
  * [Calculate LBI-TAW repertoire overlap](#calculate-lbi-taw-repertoire-overlap)
- [Evaluating song structure in bellbirds](#evaluating-song-structure-in-bellbirds)
  * [Make a subset collection for *males* on TMI:](#make-a-subset-collection-for-males-on-tmi-)
  * [Make a subset collection for *females* on TMI:](#make-a-subset-collection-for-females-on-tmi-)
  * [Produce cSPADE table and network for *males* on TMI:](#produce-cspade-table-and-network-for-males-on-tmi-)
  * [Produce cSPADE table and network for *females* on TMI:](#produce-cspade-table-and-network-for-females-on-tmi-)
  * [Compare male and female networks](#compare-male-and-female-networks)
  * [Explore male cSPADE table](#explore-male-cspade-table)
  * [Explore female cSPADE table](#explore-female-cspade-table)
- [Tutorial conclusions](#tutorial-conclusions)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>


## Getting started

To follow along in *Koe* with the same dataset:

1. Click [here](https://drive.google.com/open?id=1hiYB_-ZUsgZ4FeQVFGWm0WciqUtBFYPm) to download a zip file of database labels. 

2. Go to _Koe_ ([https://koe.io.ac.nz](https://koe.io.ac.nz)).

3. Sign in (if you aren't already).

4. Navigate to _Manage your database_.

5. Enter invitation code “KOE Case Study” (without quotes)

6. Select the **Bellbirds_Case_Study** database from the **Database** panel by clicking the round checkbox next to its name.
 
7. Click **Load ZIP** beneath the **Saved versions** panel.

8. Locate the zip file you downloaded in step 1. 

9. Click **Open**.

![](https://i.ibb.co/r7L9y3J/Loading-Label-Zip.png)


You have now loaded the label data for the units in the database and will be able to see unit labels.

***Please note: by accessing the datasets in this tutorial you agree not to use the data in any form of publication, except by express consent of the authors Wesley Webb and Yukio Fukuzawa.***



## Trying out the filter

1. Navigate to _Unit table_ view (_Classify & manage units_ > _Unit table_) 

2. Make sure that the current database is **Bellbirds_Case_Study**; select it from the **Current database** dropdown on the navigation pane if not.

Data can be explored quickly using Koe's filter, which can combine different criteria specified by a regular expression. For example, `duration:<100; sex:F; label:Downsqueak` returns only units with duration shorter than 100ms, vocalised by female birds, and label containing *Downsqueak*. Try it:

![](https://i.ibb.co/JKzvjgp/Case-Study-Filter-Before.png)
![](https://i.ibb.co/rwn7zBW/Grey-Down-Arrow.png)
![](https://i.ibb.co/RSTk3GC/Case-Study-Filter-After.png)

**Below, we use the filter to compare male and female unit diversity across the whole metapopulation, then between males at two sites.** 

# What is the overall unit diversity for male and female bellbirds across all seven sites? 

[Back to table of contents](#table-of-contents)

## Find the total number of classes

*Exemplars* view (*Classify & manage units* > *Exemplars*) displays the catalogue of unit classes, with a count of classes top left (where the arrow is pointing). This reveals **754** fine-scale classes in total: 

![](https://i.ibb.co/4JD2zm1/Case-Study-Diversity1.png)

**Now we want to see how many of the 754 are sung by males, how many by females, and how many are shared between the sexes.**

## Make a database subset for males

Make subset 'collections' by sex as follows:

1. Go to *Classify & manage units* > *Unit table* 

![](https://i.ibb.co/fXjGTrj/Case-Study-Diversity-MFSubset-1-2.png)

 
2. Type `sex:M` in the filter box to filter for all units sung by males
 
3. Select the checkbox header to select all filtered rows.

![](https://i.ibb.co/9N3nHgL/Case-Study-Diversity-MFSubset-2-2.png)

4.  Click **Make a Collection from selected units** on the active controls pane. 

![](https://i.ibb.co/QDPfky8/Case-Study-Diversity-MFSubset-3.png)

5. Type a unique name for the collection (e.g. "yourusername_Bellbirds_Males"). Note the Collection name must be unique; if the collection name has already been created (by any users, not just you), the name will not 'take'. 

![](https://i.ibb.co/X4sndkh/Case-Study-Diversity-MFSubset-4.png)

6. Click **Set**.

7. **Deselect** the selected rows by clicking the checkbox header or typing `ctrl`+*`*.

## Make a database subset for females

Make a subset for units sung by *females* in exactly the same way: 

1. Replace the filter with`sex:F` to filter for all units sung by females.
 
2. Select the checkbox header to select all filtered rows.

3. Click **Make a Collection from selected units**

4. Type a unique name for the collection (e.g. "yourusername_Bellbirds_Females")

5. Click **Set**.

6. **Deselect** the selected rows by clicking the checkbox header or typing `ctrl`+*`*.


## Find how many classes are sung by males

Go back to *Exemplars* view (_Classify & manage units_>_Exemplars_). 

1. Click on the **Current database** dropdown in the active controls pane. 

2. Select the male subset Collection you made. 

The class count at the top left (where the arrow is pointing) shows there are **517** fine-scale classes for males:

![](https://i.ibb.co/nQLTxNS/Case-Study-Diversity-All-Mal.png)


## Find how many classes are sung by females
Repeat the process for the female subset. The class count shows there are **415** fine-scale classes for females:

![](https://i.ibb.co/71kmqch/Case-Study-Diversity-All-Fem.png)

## Calculating repertoire overlap

If there are **754** fine-scale classes overall, with **517** sung by males and **415** sung by females, there must be **178** (24%) sung by both (517 + 415 – 754 = 178).

Here's another slightly more involved question:

# How many male unit types are now shared between Tawharanui and source population Hauturu?
[Back to table of contents](#table-of-contents)

![](https://i.ibb.co/KsVqhL2/LBI-TAW-Headerimage.png)

In 2005, bellbirds from Hauturu (also known as Little Barrier Island; **LBI**) naturally recolonized Tawharanui Peninsula (**TAW**) following pest control. At that point, repertoires of source and founder populations were indistinguishable (Brunton et al., 2008). After a decade of potential cultural divergence, it is of interest to assess the **current degree of repertoire overlap between the sites**.

We will do this for males.

**Note:** All our songs have filenames that start with a three-character site name (`LBI` and `TAW` in this case) followed by an `_`. We use this feature to filter for songs from different sites.

## Make a subset for males on LBI
First we will go to *Unit table* view (_Classify & manage units_ > _Unit table_) and make a 'collection' containing units sung by males from LBI:

1. Type `sex:M; song:LBI_` in the filter.

2. In the resulting unit table, select all rows by clicking the checkbox header.

3. Click **Make a Collection from selected units** on the controls pane.


![](https://i.ibb.co/Rv6fk4W/Filtering-Making-Collections-LBI.png)


4. Name the collection something logical and unique (e.g. "yourusername_LBI_M") and click **Set**. Note the Collection name must be unique; if the collection name has already been created (by any users, not just you), the name will not 'take'.
![](https://i.ibb.co/hCGJ47q/Name-Collection1.png)

5. Deselect all rows by unchecking the checkbox header, or pressing `Ctrl`+*`*


## Make a subset for males on TAW

1. Replace the filter with `sex:M; song:TAW_`

2. In the resulting unit table, select all rows by clicking the checkbox header

3. Click **Make a Collection from selected units** on the controls pane

![](https://i.ibb.co/c24y9Cg/Filtering-Making-Collections-TAW.png)

4. Name the collection something logical and unique (e.g. "yourusername_TAW_M") and click **Set**
![](https://i.ibb.co/5L0Mfcc/Name-Collection2.png)

5. Deselect all rows by unchecking the checkbox header, or pressing `Ctrl`+*`*.

## Find repertoire size for males on LBI

To find the repertoire size of the male LBI collection, go to *Exemplars* view (*Classify & manage units* > *Exemplars*):

1. Click on the current database dropdown.

2. Select your collection for LBI males, whatever you named it.

3. In the top left (where the arrow is pointing) is the count of class types in the collection. In this case, **141** male fine-scale unit classes on LBI:

![](https://i.ibb.co/dtNQL6K/Case-Study-Diversity-LBI-M.png)


4. Export the *Exemplars* view data as a `.csv` file. Click **Export entire table (csv)** on the active controls pane.

![](https://i.ibb.co/mNRnGfq/Export-Entire-Table-with-Clickerhand.png)



## Find repertoire size for males on TAW

Open the Tawharanui (TAW) male collection in *Exemplars* view (*Classify & manage units > Exemplars*) exactly as previous:

1. Click on the **Current database** dropdown

2. Select your collection for TAW males, whatever you named it

3. In this case we find 104 male fine-scale unit classes on TAW:

![](https://i.ibb.co/fpNMZ75/Case-Study-Diversity-TAW-M.png)


4. Export this *Exemplars* view data, too. Click **Export entire table (csv)** on the active controls pane.

![](https://i.ibb.co/mNRnGfq/Export-Entire-Table-with-Clickerhand.png)

## Calculate LBI-TAW repertoire overlap

The two downloaded `.csv` files will be in the downloads bar at the bottom of your browser. (You can also find them in your Downloads folder on your computer).

![](https://i.ibb.co/XFcD1PH/Downloaded-CSVs-Bottom.png)

The files contain two columns: (1) the list of classes present in the collection, and (2) the counts of those classes.

![](https://i.ibb.co/5xyF97w/Two-Lists-Side-By-Side.png)

There are several ways to find the classes shared between the two lists. You could do it in _Excel_ with formulas. Here we will read the two lists into _R_ and use `intersect` to find the classes common to both lists.

1. Read in the LBI and TAW csv files (*Note*: replace filepaths with your own), and store them as objects `LBI_Males` and `TAW_Males`:

```

LBI_Males <- read.csv("C:/Downloads/koe-exemplars-2019-03-07_15-26-57.csv",header=TRUE)

TAW_Males <- read.csv("C:/Downloads/koe-exemplars-2019-03-07_15-27-07.csv",header=TRUE)

```

2. Now we find the the classes that are common to both files. We are only interested in the first column (the list of classes) from each file; hence the `[,1]` in the code which extracts the first column: 

```

Shared_classes <- intersect(LBI_Males[,1], TAW_Males[,1])

```

3. The list of shared classes is now stored in the object `Shared_classes`, which looks like this:

```
> Shared_classes
 [1] "Chump"                           "Click"                          
 [3] "Cough(clickhigh)"                "Cough(short)"                   
 [5] "Down(slightcurve+click)"         "Downsqueak(chumpbit)_Pipe(high)"
 [7] "Ghh_Chump"                       "Pipe(A#[6])"                    
 [9] "Pipe(A#[6]+)"                    "Pipe(A#[6]bent)"                
[11] "Pipe(A[6])"                      "Pipe(A[6]+)"                    
[13] "Pipe(B[6])"                      "Pipe(B[6]+)"                    
[15] "Pipe(C[7])"                      "Pipe(D#[6])"                    
[17] "Pipe(D#[6]+)"                    "Pipe(D[6])"                     
[19] "Pipe(D[6]+)"                     "Pipe(D[6]bent)"                 
[21] "Pipe(D[7])"                      "Pipe(E[6])"                     
[23] "Pipe(F#[6])"                     "Pipe(F#[6]+)"                   
[25] "Pipe(F#[7]+)"                    "Pipe(G#[6]+)"                   
[27] "Pipe(G[6])"                      "Pipe(G[6]+)"                    
[29] "Pipe_Upslope_Pipe"               "Stutter"                        
[31] "Stutter_Stutter(LBITAW+nownow)"  "Stutter_Stutter_Stutter"        
[33] "Tink"                            "UNKNOWN"                        
[35] "Upsqueak(cleanglass)"           

```

There are 35 Tawharanui male unit classes shared with Hauturu (**34%** of the male Tawharanui population repertoire; 35/104 = 34%).

In other words, since colonization **66%** of the unit classes sung by males at Tawharanui appear to have been innovated.


# Evaluating song structure in bellbirds
[Back to table of contents](#table-of-contents)

![](https://i.ibb.co/Z6rPBMF/Network-Headerimage.png)

To help you analyse sequence structure in detail, _Mine sequence structure_ view shows the strength of association between unit classes using the cSPADE algorithm (Zaki, 2001), and produces network visualisations. 

**Here we will use _Mine sequence structure_ to compare the sequence structure of male and female bellbird song on Tiritiri Matangi Island (TMI).** 

First, [exactly as in previous sections](#what-is-the-overall-unit-diversity-for-male-and-female-bellbirds-across-all-seven-sites), we need to make collections (database subsets) for males and females on TMI. 

## Make a subset collection for *males* on TMI:

1. Go to *Unit table* view (_Classify & manage units_ > _Unit table_)

2. Type `sex:M; song:TMI_` in the filter
 
3. In the resulting unit table, select all rows by clicking the checkbox header
 
4. Click **Make a Collection from selected units** on the controls pane
 
5. Name the collection something logical and unique and click **Set**

6. Deselect all rows by unchecking the checkbox header, or pressing `Ctrl`+*`*



## Make a subset collection for *females* on TMI:

1. Replace the filter with `sex:F; song:TMI_`

2. In the resulting unit table, select all rows by clicking the checkbox header

3. Click **Make a Collection from selected units** on the controls pane

4. Name the collection something logical and unique and click **Set**

5. Deselect all rows by unchecking the checkbox header, or pressing `Ctrl`+*`*



## Produce cSPADE table and network for *males* on TMI:

1. Click on _Mine sequence structure_ in the navigation pane. 

![](https://i.ibb.co/vmkmD3m/Mine-Sequence-Structure-Button.png)



2. Click on the **Current database** dropdown.

3. Select your collection for TMI males, whatever you named it.

![](https://i.ibb.co/4dyMJsZ/Case-Study-TMISequence2.png)



You will see a table of class associations on the left, and a network visualisation on the right.

![](https://i.ibb.co/QpyGwQj/c-SPADEand-Network-1.png)

The cSPADE output table enumerates the strength of association for sequences of units. For details of the cSPADE algorithm see [this previous section](#insert-proper-hyperlink).

The interactive network visualisation shows all the 2-unit associations from the cSPADE table. The network models the direction and strength of association between pairs of units, across a population of songs (in this case, the population consists of males on TMI). 

Units are represented by nodes (the circles) which are joined by lines (edges) if the units occur _consecutively_ within songs.   The order of units is indicated by arrow direction, and strength of association between units (_lift_) is represented by edge thickness. 





Again, see [this section](#) to be reminded of definitions and [this section](#) on adjusting network appearance.

By default the network shows only those sequences that occur in at least 1% of songs. In this case, there are a high number of associations, leading to a cluttered network. We will increase the threshold to visualise only those associations that occur in **more than 5%** of songs.

4. Type `support:>0.05` in the filter box and observe how the network is now much simpler:

![](https://i.ibb.co/LpS2fYh/Case-Study-Filtering-MNetwork.png)

5. Export the filtered subset of the cSPADE table by clicking **Export filtered subset (csv)** in the active controls pane:

![](https://i.ibb.co/dfYWrTM/Export-Filtered-Subset.png)





## Produce cSPADE table and network for *females* on TMI:

We want to compare networks for males and females side-by-side, so let's duplicate the current _Koe_ browser tab to preserve the male network before we create the female network. 

1. Right-click the tab then click **Duplicate** from the dropdown menu (the menu will look different in different browsers). 

![](https://i.ibb.co/bRVC4qn/Duplicate-Seq-Mining-Tab.png)

2. If you are using two computer monitors, drag the new tab to the second monitor, so that you can see both simultaneously. One tab will be for the male network (already produced) and the other for the female network.

3. On the tab you want to produce the female network, click on the **Current database** dropdown.

4. Select your collection for TMI females, whatever you named it.

Similarly to the male network, at the default threshold of 1% occurrence (present in at least 1% of songs), the network is cluttered with many associations: 
![](https://i.ibb.co/MRNhKmN/c-SPADEand-Network-Fem.png)

To be comparable with the male network, we will increase the threshold to visualise only those associations that occur in **more than 5%** of songs.

5. Type `support:>0.05` in the filter box

![](https://i.ibb.co/2MqXCrg/Case-Study-Filtering-FNetwork.png)

6. Export the filtered subset of the cSPADE table by clicking **Export filtered subset (csv)** in the active controls pane:

![](https://i.ibb.co/dfYWrTM/Export-Filtered-Subset.png)

## Compare male and female networks

![](https://i.ibb.co/wBQNBSc/Male-Female-Network.png)


At this threshold, the songs of both sexes contain some nodes with many connections; these unit classes (e.g. _Dragon_ in males, _Stutter_ in females) can be preceded/followed by many different classes. 

Both sexes also contain nodes which are strictly preceded/followed by a certain class; for example, in males _Waah(mid+A)_ is always followed by _Dragon_, and in females _Peakwhistle(TMI)_ is always preceded by _Stutter_.  

We can see that both sexes sing repeated units, represented by looped lines: 

**For males**: _Dragon_, _Stutter_, _Cough(TMI+click)_ 
**For females**: _Stutter_, _Stutter(wavey)_, _Pipe(D#[7]+)_, _Pipe(E[7])_ 

A notable difference in the female network is this chain of strongly connected nodes, upper left-hand-side of the graph: 

`Killem` → `Pipe(C#[7]+)` → `Upsqueak_Flatsqueak(1)` → `Downsqueak(twopart)` → `Down_Click_Stepdown` → `Stepdown(C[7]-C[6])`.

The thick lines between these pairs of classes on the graph indicate high values of _lift_; that is, each two-unit association occurs much more often than would be expected by chance. Note this does not necessarily imply that the entire chain occurs in any one song, but rather that each consecutive pair is strongly associated.

## Explore male cSPADE table

1. Find the male cSPADE table `csv` file you previously exported. It will be in your computer's Downloads folder.

2. Open it in *Excel*

3. Sort the table by the **chainlength** column from lowest to highest, then secondarily by the **support** column from highest to lowest:

![](https://i.ibb.co/YWzM8jN/Sort-Excel.png)


The sorted data should look like this:

![](https://i.ibb.co/TWKWYg4/Malec-SPADEin-Excel-1.png)


These associations at the top of the table (with chain length of 1) are not true associations *per se*, as they are only one unit long. They give useful information about how the number and proportion of songs those unit classes occur in (transcount and support columns, respectively). However, confidence and lift values cannot be calculated because these require associations with two or more units (hence the nonsensical **-1** values in these columns). 

`__PSEUDO_START__` and `__PSEUDO_END__` are not true classes, but mark the start and end points of the song. As every song has a start and end, both have a support of **1** (meaning they occur in 100% of songs).

The third row of the table shows that `Dragon` occurs in 201 songs (transcount column), which is 51.7% of all the songs in the male TMI population (support column). By this measure it is the most prevalent male syllable class on TMI; next most prevalent are `Cough(TMI+click)` (40.1% of songs), `Downsqueak(hook)` (34.7% of songs), and so on down the list.

3. Scroll down or filter the table to find associations with a chain length of 2. These are the associations visualised in the network diagram.

![](https://i.ibb.co/Twdpk0X/Malec-SPADEin-Excel-2.png)


The sequence: 

`Cough(TMI+click)` ⇒ `Downsqueak(hook)`

has a **support** of 0.32, which means this sequence occurs in 32% of songs. 

It has a **confidence** of 0.81, which means that when `Cough(TMI+click)` occurs, `Downsqueak(hook)` comes next in 81% of songs. 

It has a **lift** of 2.33, which means that `Downsqueak(hook)` follows `Cough(TMI+click)` in 2.33 times the number of songs as expected by chance.

**Note**: In the notation of Zaki (2001) this association would be written
[(`Cough(TMI+click)`)]⇒[(`Cough(TMI+click)`)(`Downsqueak(hook)`)]


***Male song tends to start with one of four syllable types***

By looking at two-unit associations beginning with `__PSEUDO_START__`, we can see which syllables tend to occur at the start of male songs:

The 'sequence'

`__PSEUDO_START__` ⇒ `Stutter` 

has a **support** of 0.29, which means that in 29% of songs in this male population, `__PSEUDO_START__` ⇒ `Stutter` occurs (that is, `Stutter` is the starting syllable).

It also has a **confidence** of 0.29, which means given `__PSEUDO_START__`, `Stutter` follows in 29% of songs (in this case, this means the same as support).

It has a **lift** of 0.95, which means that `Stutter` follows `__PSEUDO_START__` in 95% as many songs as expected by chance, based on the frequency of `Stutter` in the dataset.

The other three starting syllables are: 

`__PSEUDO_START__` ⇒ `Cough(TMI+click)` (support=0.23, confidence=0.23, lift=0.57)

`__PSEUDO_START__` ⇒ `Downsqueak(bitunder)_Pipe(low)` (support=0.10, confidence=0.10, lift=0.45)

`__PSEUDO_START__` ⇒ ` Waah(rough)` (support=0.08, confidence=0.08, lift=0.30)


***Three syllable types tend to end male song***

By looking at two-unit associations ending with `__PSEUDO_END__`, we can see which syllables tend to occur at the end of male songs:

`Moustache` ⇒ `__PSEUDO_END__` (support=0.12, confidence=0.81, lift=0.81)

`Dragon` ⇒ `__PSEUDO_END__` (support=0.30, confidence=0.57, lift=0.57)

`Cough(TMI+click)` ⇒ `__PSEUDO_END__` (support=0.12, confidence=0.29, lift=0.29)

4. Scroll down the table to find associations with a chain length of 3.

![](https://i.ibb.co/P9XNV13/Malec-SPADEin-Excel-3.png)

The sequence: 

`Trill ⇒ Dragon` ⇒ `Moustache`

has a **support** of 0.08, which means this sequence occurs in 8% of songs. 

It has a **confidence** of 0.86, which means that when `Trill ⇒ Dragon` occurs, `Moustache` comes next in 86% of songs. 

It has a **lift** of 5.9, which means that `Moustache` follows `Trill ⇒ Dragon` in 5.9 times the number of songs as expected by chance.

**Note**: In the notation of Zaki (2001) this association would be written
[(`Trill`)(`Dragon`)]⇒[(`Trill`)(`Dragon`)(`Moustache`)]



## Explore female cSPADE table

1. Find the female cSPADE table `csv` file you previously exported. It will be in your computer's Downloads folder.

2. Open it in *Excel*

3. Sort the table by the **chainlength** column from lowest to highest, then secondarily by the **support** column from highest to lowest:

![](https://i.ibb.co/YWzM8jN/Sort-Excel.png)


The sorted data should look like this:

![](https://i.ibb.co/Y0Rj4Qv/Femalec-SPADEin-Excel-1.png)

The third row of the table shows that `Stutter` occurs in 129 songs (transcount column), which is 93.4% of all the songs in the female TMI population (support column). By this measure it is the most prevalent female syllable class on TMI (compared to 51.7% for the most prevalent class in males).

The next most prevalent female classes are `Chiup` (59.4% of songs), `Downcurve(doublevoiced)` (36.2% of songs), and so on down the list.

3. Scroll down to find associations with a chain length of 2. These are the associations visualised in the network diagram.

![](https://i.ibb.co/yyKCWr8/Femalec-SPADEin-Excel-2.png)

Here we can see the importance of `Stutter` syllable types for the structure of female bellbird song.

***Stutter almost always starts female songs***

`__PSEUDO_START__` ⇒ `Stutter`

has a **support** of 0.91, which means that in 91% of songs in this population, `Stutter` is the starting syllable.

It also has a **confidence** of 0.91, which means given the start of a song (`__PSEUDO_START__`), `Stutter` follows in 91% of cases.

It has a **lift** of 0.97, which means that `Stutter` follows `__PSEUDO_START__` 97% as often as expected by chance.




***Stutter tends to repeat in female songs***

`Stutter` ⇒ `Stutter` is common (support=0.85, confidence=0.91, lift=0.97).

In fact, if we scroll down the table we see that `Stutter` is commonly repeated many times:

![](https://i.ibb.co/9whfNJ9/Femalec-SPADEin-Excel-3.png)

For example, 

`Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter` ⇒ `Stutter` 

occurs in 29% of songs

`Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter ⇒ Stutter` ⇒ `Stutter`

occurs in 15% of songs.


***Stutter sometimes ends female songs***

`Stutter` ⇒ `__PSUEDO_END__` occurs in 38% of songs (support=0.38, confidence=0.40, lift=0.40).


# Tutorial conclusions
[Back to table of contents](#table-of-contents)

These examples have illustrated a some simple ways to assess unit repertoire size and repertoire sharing, and demonstrated how to examine sequence structure using the cSPADE algorithm and network visualisations. Data exported from _Koe_ enable many more kinds of analyses in other software. 

For example:

* *EstimateS* ([http://viceroy.eeb.uconn.edu/estimates/](http://viceroy.eeb.uconn.edu/estimates/)) can be used to estimate total unit richness in a population by robustly extrapolating from the _Koe_ classification data. 

* From the unit features extracted by _Koe_, distributions of unit features could be plotted in *R* or *Python* and compared between groups

* In _Excel_ unusual syntax could be identified in the cSPADE table as one means of identifying potential classification errors


----------------

{{% children depth=999 %}}
