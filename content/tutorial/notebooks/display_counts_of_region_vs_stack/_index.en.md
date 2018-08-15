---
title: Display Counts of ROI vs Stack
post: " <i class='fa fa-battery-2'></i>"
---

**Notebook name**: display_counts_of_region_vs_stack.ipynb

## Description

In this notebook, you will be able to get the average number of counts of a given region
vs all the images of the selected folder.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select the Images

Select **the folder** containing the images you want to process using the **File Selector**. 
The images will then be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/file_selector/images/select_folder.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

### Launch the UI

**SHIFT** + **ENTER** in the next cell (**Launch UI**) to start the interface.

## UI Presentation

<img src='/tutorial/notebooks/display_counts_of_region_vs_stack/images/ui_general.png' />

### Region of Interest (ROI)

By default, a ROI is already defined for you in the top left corner of the preview region. 

To move it, click inside the ROI (edges will turn yellow). 
To resize it, grab the bottom right corner and move it to resize it.

The Average counts of this entire region, for all the images from the folder, will be displayed live at the bottom
of the interface.

<img src='/tutorial/notebooks/display_counts_of_region_vs_stack/images/roi_selection.gif' />

### Time Spectra (OPTIONAL)

<img src='/images/comingsoon.png' />
