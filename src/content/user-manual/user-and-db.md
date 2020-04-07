+++
title = "User and database control"
date = 2020-04-03T12:34:36+13:00
weight = 4
pre = "<b>1.4 </b>"
disableToc = true
+++

Create an account
---

Go to [koe.io.ac.nz](https://koe.io.ac.nz) and click on **Register** to register an account. 

Choose a username, input your name and email address for purposes of _Koe_ support correspondence, and choose a password. (We will never share your information with anyone).
  
![](https://i.ibb.co/xD1nLZ1/Sign-Up-Code-Removed.png)

Create a new database
---
[Back to table of contents](#table-of-contents)

Under Manage your database, click **New database** to create a new database.
 

![](https://i.ibb.co/0fSKJj6/Manage-Database.png)

Add collaborators to a database and set permission levels
---
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
