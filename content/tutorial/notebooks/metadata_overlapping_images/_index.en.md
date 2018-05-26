---
title: Metatadata Overlapping Images
post: "<i class='fa fa-battery-empty'></i> "
---

**Notebook name**: metadata_overlapping_images.ipynb

## Description

This notebook normalized the imaging data (tiff or fits) by removing the background and fixing the fluctuations of the
neutron beam. You will need:

 * select your images
 * select your open beam (OB)
 * optional - select the dark field (DF)
 * optional - select one or more background region in your sample images
 * run the normalization
 * select output folder where the normalized images will be saved

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Images

You need to provide the list of **samples**, **OB** and **DF** (if needed). To do so, just **SHIFT + ENTER** the
following cell to display a *selection tool wizard*.

<img src='/tutorial/notebooks/normalization_live/images/loading_images_1.gif' />

The dialogbox will start listing the files from the IPTS folder you selected in the first cell. Feel free to navigate
to find your data set.

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

<img src='/images/comingsoon.png' />


