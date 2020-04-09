+++
title = "Frequently Asked Questions"
date = 2020-04-03T12:34:36+13:00
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

![](https://i.ibb.co/ZXq8K40/vlad-tchompalov-ku-TZUOVRp-Oo-unsplash-PARROT1.png)

# How do I report bugs or suggest features?
Your bug reporting and feature requests help us make *Koe* a joy to use!

Live chat with us at our Facebook page [www.facebook.com/KoeSoftware](www.facebook.com/KoeSoftware). Alternatively, send us an email at [koe@io.ac.nz](mailto:koe@io.ac.nz). Check out the current list of known bugs and feature requests under the [**Issues**](https://github.com/fzyukio/koe/issues) tab in GitHub. 
 

# Can I install *Koe* on my local machine?
Yes you can, but it will take a wee bit of coding know-how to set it up. See:  [https://github.com/fzyukio/koe#how-to-install-run-and-deploy-this-on-your-own](https://github.com/fzyukio/koe#how-to-install-run-and-deploy-this-on-your-own)

# I'm missing certain buttons on the navigation pane...

If you don't see certain buttons, e.g. 'Upload & split raw recordings' or 'Upload songs' (left hand side of the screen), it's probably because the database is owned by another user and they haven't granted you full permissions. 

For instructions on how to grant permissions, see: https://github.com/fzyukio/koe/wiki#add-collaborators-to-a-database-and-set-permission-levels  


# How can I adjust spectrogram settings to suit the Hz range of my species?
Currently you can adjust spectrogram colourmap, contrast, and time-axis zoom. We recognise the need to be able to specify spectrogram floor/ceiling, especially for species with low-pitched vocalisations. We are working on expanding the range of spectrogram settings. Contact us to tell us more about the requirements of your species, so that we can make sure _Koe_ is useful for you.

# I have already segmented units in other software. Can I import this information into *Koe*?
Rejoice! You can import segmentation data as unit start/end-points in a csv file, thereby avoiding having to re-segment units in *Koe*. 

See [https://github.com/fzyukio/koe/wiki#import-unit-segmentation-from-csv](https://github.com/fzyukio/koe/wiki#import-unit-segmentation-from-csv)

# How do I get my tSNE ordination to cluster nicely?
How clustered your data appears in the ordination (*Classify & manage units* > *Ordination*) will depend on a few things:

**The set of unit features you extract** 
This is what is used to calculate unit similarity. Some combinations of features may be better at separating unit categories than others.

**The value of 'perplexity' you set for the tSNE**
 tSNE has a global variable called 'perplexity' which influences the  appearance of the ordination. This variable is used universally for all data points. A small value can cause bona fide clusters to break up, a big value can lead to several clusters being put together.

**How many data points you have**
Sometimes, having many thousands of data points can result in a big cloud-like blob rather than neat clusters.

----
***Here are some things to try:***  

-- Change which unit features are extracted. If in doubt, extract all features, using all aggregation methods ([https://github.com/fzyukio/koe/wiki#extract-unit-features](https://github.com/fzyukio/koe/wiki#extract-unit-features)).

-- Try changing the value of the 'perplexity' variable ([https://github.com/fzyukio/koe/wiki#construct-ordination](https://github.com/fzyukio/koe/wiki#construct-ordination))

-- If you are experiencing some good clusters, but other regions of the ordination are a 'big blob', try this: 

1. Make a selection of the big blob in the ordination
2. Click the **View table** button, which will open a *Unit table* containing only the selected units. 
3. Click on the top checkbox button to select all those units
4. Click **Make collection from selected units** on the left hand panel. 

Now you can use this collection as a database and run feature extraction with different features—and ordination with different values of perplexity—to see if the cloud of points can break up into clusters.
