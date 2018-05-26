---
title: Profile
post: "<i class='fa fa-battery-full'></i> "
---

**Notebook name**: profile.ipynb

## Description

We created this notebook to get very precise profile of samples. For example, if you want to select a profile of
exactly the center of your cylindrical sample, then this notebook is for you.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Images to Process

Select the images you want to process using the **File Selector**. Once you **click** the **Select** button, the time
stamp and the images will be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/calibrated_transmission/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## Profile UI Presentation

<img src='/tutorial/notebooks/profile/images/tab1_ui_presentation.png' />
<img src='/tutorial/notebooks/profile/images/tab3_ui_presentation.png' />
<img src='/tutorial/notebooks/profile/images/tab2_ui_presentation.png' />

## How Does it Work ?

### Tool to Help you Select the Profile(s)

The **guide** (red box surrounding the profile) is only there to help you define and move your **profile** with
precision. Once the profile has been defined, **disable** the guide to **lock** the position of the profile.

<img src='/tutorial/notebooks/profile/images/profile_selection.gif' />

### Profiles Plots

The profile plots of the current image selected are displayed at the bottom of the interface.

<img src='/tutorial/notebooks/profile/images/live_profile_plots.gif' />

### All Profiles / All Images

By going to the tab **All Profiles / All Images**, you can display on the same plot the profiles you select with the
images you select.

<img src='/tutorial/notebooks/profile/images/all_plots_all_files.png' />

### Export Profiles

After clicking the **Export Profiles...** button, and selecting an output folder, each profile will produce an ascii file.
The top of this ascii file contains some metadata such as size of profile, list of input file name....
Then the profile for each file will be saved into a comma separated table where each column is a file.

<img src='/tutorial/notebooks/profile/images/export_file.png' />
