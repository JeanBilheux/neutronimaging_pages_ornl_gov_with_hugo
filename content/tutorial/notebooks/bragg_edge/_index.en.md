---
title: Bragg Edge
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge.ipynb

## Description

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Normalized Images

You need to provide the list of **samples**, **OB** and **DF** (if needed). To do so, just **SHIFT + ENTER** the
following cell to display a *selection tool wizard*.

<img src='/tutorial/notebooks/calibrated_transmission/images/select_files.gif' />

The dialogbox will start listing the files from the IPTS folder you selected in the first cell. Feel free to navigate
to find your data set.

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

### Presentation of the UI

<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/presentation_of_main_ui.png' />
<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/presentation_of_second_tab.png' />

### Step by Step

#### ROI selection

You have the option with this UI to select more than one region of interest (ROI). Click the **+** button on the right
to add a ROI, and **-** if you want to remove the ROI selected. You can also **enabled** or **disabled** any of the
ROIs.

To modify any of the ROI, you can either:

 * **move** or **resize** the ROI directly from the Image window
 * manually change x0, y0, width or/and height in the ROI table

The **total conts vs file index** plot will be updated live as you modified the ROI.
This plot displays the **mean** or **total counts** of the ROIs for each image (1 image = 1 data point)

<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/roi_table.gif' />

#### Integration Algorithm

The current implementation provides 2 algorithms to integrate the counts within each ROI

 * Add - sum counts of all the pixels in the ROI
 * Mean - average counts of all the pixels in the ROI

The **total counts vs file index** plot will be updated live as you change the algorithm.

#### Export the Counts vs file name and time stamp information

Click the **Export Counts vs File Name and Time Stamp ...** button to create the ascii file version of the data found
int the **Summary Tab** table.

The following 3 images shows an example where 3 ROIs have been created, how the **summary tab** looks like and the final
output file created.

<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/main_tab_before_export.png' />
<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/summary_tab.png' />
<img src='/tutorial/notebooks/integrated_roi_counts_vs_file_name_and_time_stamp/images/export_file.png' />
