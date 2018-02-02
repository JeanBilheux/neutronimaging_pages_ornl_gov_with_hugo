---
title: Access your data
weight: 210
---

<h2 id='top'></h2>

This will require that you complete 2 steps:

 * <a href='#create_account'>Step 1: request access to our computer</a>
 * <a href='#reach_data'>Step 2: reach your data</a>

<h2 id='create_account'>
## <a href='#top' class='fa fa-arrow-up'></a> Step 1. Request access to our computers

**1.** Create an XCAMS account

If you have not done so, please create an [XCAMS account](https://xcams.ornl.gov/xcams/groups/prpsl_user/index.shtml)
<img src='/tutorial/how_to_access_data/images/ipts_access.png' />

**2.** Request access to HFIR data

You can request access to your data by visiting this page [https://neutronsr.us/accounts/request.html](https://neutronsr.us/accounts/request.html)
<img src='/tutorial/how_to_access_data/images/hfir_access.png' />

<a href='#top'>TOP</a>
<h2 id='reach_data'></h2>
## <a href='#top' class='fa fa-arrow-up'></a> Step 2. Reach your data

If the goal is to bring your data to your computer for local visualization and analysis -**not recommended due to the size of the data
and the tools we offer via our analysis computer** - you can either use:

<ul>
  <li><a href='#filezilla'>FileZilla</a></li>
  <li><a href='#cyberduck'>Cyberduck</a></li>
</ul>

<h2 id='filezilla'></h2>
### Using FileZilla

**1.** Install [FileZilla](https://sourceforge.net/projects/filezilla).

**2** Create and configure a new bookmark

<img src='/tutorial/how_to_access_data/images/filezilla_bookmark.png' />

Enter the information as followed:

 * **Host**: *analysis.sns.gov*
 * **Port**: *22*
 * **Protocol**: Select *SFTP - SSH File Transfer Protocol*
 * **Logon Type**: *Normal*
 * **User**: *\<your xcams>*
 * **Password**: *\<your password>*

 Click **Connect**

<img src='/tutorial/how_to_access_data/images/filezilla_configure.png' />

You can now browse to your data by following the structure **/HFIR/CG1D/IPTS-XXXX**

<img src='/tutorial/how_to_access_data/images/filezilla_browse.png' />

**3.** Import Data

If you want to copy your data to your local computer, simply **DRAG** and **DROP** the folder of interest into your
*Desktop* display on the left side of the window.

<img src='/tutorial/how_to_access_data/images/filezilla_export.gif' />



<h2 id='cyberduck'></h2>
### Using Cyberduck

**1.** Install [Cyberduck](https://cyberduck.io/).

**2.** Create and configure a new bookmark

<img src='/tutorial/how_to_access_data/images/cyberduck_bookmark.png' />

Enter the information as followed:

 * *SFTP (SSH File Transfer Protocol)*
 * **Server**: *analysis.sns.gov*
 * **Port**: *22*
 * **Username**: *\<your xcams>*
 * **Password**: *\<your password>*
 * **SSH Private Key**: *None*

 Click **Connect**

<img src='/tutorial/how_to_access_data/images/cyberduck_configure.png' />

You can now browse to your data by following the structure **/HFIR/CG1D/IPTS-XXXX**

<img src='/tutorial/how_to_access_data/images/cyberduck_browse.png' />

**3.** Import Data

If you want to copy your data to your local computer, simply **DRAG** and **DROP** the folder of interest into your
*Desktop*.

<img src='/tutorial/how_to_access_data/images/cyberduck_export.gif' />

### File Structure

If you get lost in the file system, here is a typical map of the file structure.

<img src='/tutorial/how_to_access_data/images/file_structure.png' />



<a href='#top' class='fa fa-arrow-up'></a>
