---
title: Bragg Edge Normalization
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_normalization.ipynb

## Description

This notebook is dedicated to the normalization of data set taken at the SNS.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Prepare UI Engine

{{% notice warning %}}
Make sure you don't forget to run this cell (**Prepare UI engine**) if you want to select a region of interest later 
in the notebook.
{{% /notice %}}

### Select Raw Data Input Folder

Select the **sample folder** using the file selector. If the **time spectra** file is part of the folder, it will 
be automatically loaded, if **not**, you will have the option to manually select the **time spectra** file next, 
or just ignore it and click the button **dot not select any time spectra**

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

{{% notice info %}}
If you select a time spectra file, it will be automatically copied into the output folder. this will facilitate
the next step that is usually the extraction of the Bragg edges versus lambda/TOF into an ASCII file.
{{% /notice %}}

<img src='/tutorial/notebooks/bragg_edge_normalization/images/load_data.gif' />

The sample data will be automatically loaded and a message will inform you of the number of files loaded and
the status of the time spectra file.

### Select mode of normalization

You will have now the option to perform the normalization using two modes:

 * using **open beam**
 * using **background region of sample**

#### With open beam

<img src='/tutorial/notebooks/bragg_edge_normalization/images/with_ob_preview.png' />

 * Select first the **OB** folder by clicking **Select OB ...**
 * The slider defines the number of images to use in the preview to select the ROI. The higher the number of images,
 the better the contrast, but the slower the loading.
 * OPTIONAL: Select a **region of interest (ROI)** ([ROI selection tool tutorial here](/tutorial/notebooks/roi_selection_tool/))

 {{% notice warning %}}
Select a region away from the sample
{{% /notice %}}
 
<img src='/tutorial/notebooks/bragg_edge_normalization/images/with_ob_demo.gif' /> 

#### Without open beam

<img src='/tutorial/notebooks/bragg_edge_normalization/images/without_ob_preview.png' />
 
 * The slider defines the number of images to use in the preview to select the ROI. The higher the number of images,
 the better the contrast, but the slower the loading.
 * MANDATORY: Select a **region of interest (ROI)** ([ROI selection tool tutorial here](/tutorial/notebooks/roi_selection_tool/))

{{% notice warning %}}
Select a region away from the sample
{{% /notice %}}

<img src='/tutorial/notebooks/bragg_edge_normalization/images/without_ob_demo.gif' /> 

### Export Normalized Data and Time Spectra File

After running this cell, you will be asked to select the output folder to use to create the normalized images.

<img src='/tutorial/notebooks/bragg_edge_normalization/images/export.gif' />
