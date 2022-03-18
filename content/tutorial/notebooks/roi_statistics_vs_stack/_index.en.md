---
title: Roi Statistics vs Stack
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

## Description

Notebook to display and export statistics of region of interest selected (ROI) over all images loaded.

## How does it work

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Folder of Images to Process

Select the folder containing the data to load. All the data, of the most dominant extension, will be loaded when
launching the user interface, in the next step.

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

### Launch the User Interface (UI)

Run the next cell to launch the UI.

<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/user_interface_1.png' />
<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/user_interface_2.png' />

### ROI

In order to move the region of interest (ROI), simply click and drag anywhere on the blue line of the ROI. To resize
it, click and drag the bottom right corner of the ROI. Any changes to the ROI will reset the **table content** and the
**plots**. Click the **Recalculate Table** button to update the table and plots.

<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/roi.gif' />

### Statistics

#### Table

The statistics table has the following columns:

 - file name: without the path
 - time offset: relative to the first image, in seconds
 - min: pixel counts within the ROI having the minimum counts
 - max: pixel counts within the ROI having the maximum counts
 - mean: mean of counts within the ROI
 - median: median of counts within the ROI
 - std: standard deviation of counts within the ROI
 
#### Plot

You can select the x-axis to choose

 - file index
 - time offset (s)
 
and any y-axis

 - min
 - max
 - mean
 - median
 - std

### File Index

Any selection of a row in the table, or moving the file index slider will update the main plot and display the 
current selected image. 

<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/file_index.gif' />

### Export

Click the **Export ...** button to create an ASCII (CSV, comma separated format) file in the folder location you specify.

{{% notice info %}}
If the **Export ...** button is disabled, click first **Recalculate Table**.
{{% /notice %}}

The file name created will be based on the input folder + **_statistics.txt** 

<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/ascii.png' />

The bottom left status bar of the UI will let you know the location and full name of the file you just created.

<img src='/tutorial/notebooks/roi_statistics_vs_stack/images/status_message.png' />
