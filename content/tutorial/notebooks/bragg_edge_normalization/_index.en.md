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
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Sample Folder

Select the **sample folder** using the file selector. If the **time spectra** file is part of the folder, it will 
be automatically loaded, if **not**, you will have the option to select the **time spectra** file next, or just ignore 
it and click the button **dot not select any time spectra**

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

The sample data will be automatically loaded.

### Select OB Folder

Just like you did for the sample data, select the folder containing the open beam (OB) data. Once you selected this
folder the data will be automatically loaded.

### Selection of background region in the image

You have the option to define a region of your image that **is background** for sure. This will improve the normalization.

To do so, you first need to specify how many random images you want to use to help the selection. The more images
you select, the higher resolution your image will have but the longer it will take to display it. Usually the 
default number of images provided is a good compromise. If you can not see your sample in the image, just close the UI and 
increase the number of images to use.

Once the **ROI selection tool UI** show up, you can select, or not, 1 or more regions. You need to make sure that/those 
region(s) is/are away from the sample. If the sample covers the entire image, do not select any region!
 Once you are done, **click OK** to close the UI.

**Remember** The more images you want to load, the longer it will take. 

<img src='/tutorial/notebooks/bragg_edge_normalization/images/how_many_images.png' />

<img src='/tutorial/notebooks/bragg_edge_normalization/images/select_sample_roi.gif' />

### Perform normalization

Just run this cell to run the normalization algorithm. 

### Export normalized data

Select where you want to export all the normalized images. You have the option to create a folder if needed. The
notebook will create a folder inside the output folder location you selected. The folder will be named after the
input sample folder name. If input folder is *test_data*, the normalized folder will be *test_data_normalized*

<img src='/tutorial/notebooks/bragg_edge_normalization/images/export_data.gif' />

If you selected, or if the program automatically found, a **time spectra file**, this file will be copied into the output 
folder. 
