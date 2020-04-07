+++
title = "Songs control"
date = 2020-04-03T12:34:36+13:00
weight = 5
pre = "<b>1.5 </b>"
disableToc = true
+++

Upload songs
---

[*Click this link to download NZ bellbird songs to try out **Upload songs** feature and subsequent steps*](https://drive.google.com/open?id=1fEyWtzjim-32KNtisl1cXWcilCgxdHLR)

If you have already-divided song files on your computer, you can upload these directly. On the navigation pane, click **Upload songs** and select up to 100 WAV files at once to upload. 

 ![](https://i.ibb.co/t8hLv6c/Upload-Songs.png)

For raw recordings that need to be divided into songs, see next step.

Upload raw recordings and divide into songs
---

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

{{% notice info %}}
Recordings too big to upload? Use this tool to automatically split your wav files
{{% /notice %}}
Some bioacoustics researchers work with looong recordings (e.g. passive acoustic monitoring). Very large files can be cumbersome. But don't worry! Yukio Fukuzawa has heard your cries and has come galloping to our rescue with a simple tool for automatically splitting large wav files into smaller wav files. You specify how long you want the audio sections to be, and how many seconds of overlap between sections. 

To run the tool you will need to install Python. After that it's just a simple line of code that you type into your command prompt.

The tool and instructions are found here: [https://github.com/fzyukio/split-songs](https://github.com/fzyukio/split-songs)
