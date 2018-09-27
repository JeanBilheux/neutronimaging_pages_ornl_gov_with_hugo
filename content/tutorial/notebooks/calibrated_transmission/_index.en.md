---
title: Calibrated Transmission
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: calibrated_transmission.ipynb

## Description

The goal of this notebook is to display the average counts of region selected for each file. It's possible to calibrate
up to 2 regions by giving them a value. If a region with a mean counts of 100 is calibrated to 1 for example, all the
other value displayed will use this new scaled defined. That means, if for a file the mean counts of a region is 200,
the program will display 2. When 2 calibrated region are defined, a linear interpolation is used to dislay the mean
counts of the region selected. When no calibrated region have been defined, the true (raw) mean counts are displayed.

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

## Calibrated Transmission UI Presentation

<img src='/tutorial/notebooks/calibrated_transmission/images/presentation_of_ui_1.png' />
<img src='/tutorial/notebooks/calibrated_transmission/images/presentation_of_ui_2.png' />

## How Does it Work ?

### Define the Calibration Regions

 * Activate or deactivate the calibration region you want/do not want.
 * Define the position and size of the region (using mouse in the image viewer, or by manual input)
 * Select the value corresponding to this region
 * Select the file to use corresponding to that region

<img src='/tutorial/notebooks/calibrated_transmission/images/calibration_definition.gif' />

### Define the Measurement Regions

 * Go the **Measurement Regions** tab
 * Add new regions by clicking the **+** button at the bottom right
 * Change the position (using mouse in image viewer or by manual input in the table)
 * Remove regions using the **-** button

<img src='/tutorial/notebooks/calibrated_transmission/images/measurement_definition.gif' />

### Summary Tab

The Summary tab display the list of files, time stamp, relative time (using the first file as reference or time 0),
and mean counts calibrated for each measurement regions.

<img src='/tutorial/notebooks/calibrated_transmission/images/summary.png' />

### Export Calibrated Transmission

You can now export the calibrated transmission signal for each file by clicking the **Export Calibrated Transmission**
button. Just select the output location. The file name created will be based on the input data folder and will look like this.

If input data file is **light_loop1_flow2**, the output file will be named **light_loop1_flow2_calibrated_transmission.txt**

<img src='/tutorial/notebooks/calibrated_transmission/images/output_file.png' />