+++
title = "What's new in Koe?"
date = 2020-04-03T12:34:36+13:00
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

![Photo by Anders Jacobsen on Unsplash](https://i.ibb.co/3zzb5x9/anders-jacobsen-4-RC-a-A6xr-Ys-unsplash-HIPPO1.png)

### *We update this page regularly to report new features and bug fixes.*

# 06/04/2020
**Added keyboard shortcuts section to wiki** 
(https://github.com/fzyukio/koe/wiki#keyboard-shortcuts)




# 01/04/2020 — New Release — Version 5.4.1

## New stuff

**–Report bugs or suggest features** by chatting with us directly at facebook.com/KoeSoftware (just hit the [Send message](https://www.messenger.com/t/KoeSoftware) button). You can still email us at [koe@io.ac.nz](mailto:koe.io.ac.nz) if you prefer.

**–A new Frequently Asked Questions page** (https://github.com/fzyukio/koe/wiki/Frequently-Asked-Questions). We will update this regularly.

**–Import unit segmentation start/end points.** If you have already segmented units using other software, you can import the unit segmentation start/end point data into _Koe_, and avoid doing it over again in _Koe_. This is now properly documented on the wiki: https://github.com/fzyukio/koe/wiki#import-unit-segmentation-from-csv

**–Automatically split long wav files into smaller chunks**. Some of us work with very long, cumbersome recordings. Yukio has made a handy tool which allows you to automatically split long wav files into sections of specified length, with a specified amount of overlap between sections. This is a standalone tool, not inside of Koe (because it runs on your computer, not in your browser). To run the tool you will need to install Python. After that it's just a simple line of code that you type into your command prompt. The tool and instructions are here: https://github.com/fzyukio/split-songs

**–Database hierarchy makes more sense.** If you change 'sex' or 'species' column info associated with an individual animal, the changes will be reflected for all rows in the table belonging to that individual (you may need to refresh your browser to see the change propagate). This prevents mistakes, such as the same individual being ascribed male sex in some rows and female sex in other rows. It also means you only have to enter sex and species information for an individual in one row, saving time. 

**–New 'Added' data column—to record the date a recording was added to the database.** Handy for finding recent files versus files added a long time ago.

**–Filter data by date.** You can now filter your data in *Classify & manage units* > *Unit table* by date in 'Date of record' and 'Added' columns. Use this format, e.g. `date: from(2015-01-01)to(2018-12-31)`


**–Users can now delete databases**


**–Species name column is no longer constrained to two-part "Genus species" naming scheme; name species any way you want**

## Fixed stuff

**–Audio upload issues are fixed.** This includes issues with uploading large files.  

**–Audio playback issues are fixed.** Audio sometimes did not play in _View all songs_

**–Missing spectrograms issue is fixed.** Some users experienced missing spectrograms.

**–Download songs button (in _View all songs_) is fixed**

**–Manually re-ordered columns now keep their custom order after refresh**

## Stuff in the works

**–An installer package for using _Koe_ locally.** Installing Koe on your local machine has several advantages. You will not be dependent on an internet connection, and tasks will be performed on your computer rather than on the Koe server, which can lead to improved performance. _Koe_ can already be installed on your local computer (see https://github.com/fzyukio/koe#how-to-install-run-and-deploy-this-on-your-own), but we recognise that some users may find setup a little daunting. So we are planning an installer package that will make it simpler to get going with _Koe_ on your own.