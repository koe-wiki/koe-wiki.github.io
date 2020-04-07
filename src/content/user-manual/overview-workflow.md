+++
title = "Overview of Koe workflow"
date = 2020-04-03T12:34:36+13:00
weight = 2
pre = "<b>1.2 </b>"
disableToc = true
+++

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
