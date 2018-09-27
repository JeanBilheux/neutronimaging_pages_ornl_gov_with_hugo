---
title: List TIFF Metadata
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: list_tiff_metadata.ipynb

## Description

This notebook will list the value of the metadata you selected for the full stack of images you loaded. You will
then have the option to export this table in an ascii (comma separeated) file.

 * select your tiff images
 * select the metadata you want to see
 * metadata are listed
 * (OPTION) select folder to export the table

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select TIFF images

Select the list of tiff images using the file selector

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

### Select metadata to display

Using the first image selected, the program will determine the list of metadata available and will display the list here.
Select the one you want to output.

<img src='/tutorial/notebooks/list_tiff_metadata/images/select_metadata.gif' />

### Metadat displayed

The selected metadata value for all the images is displayed in a dropdown list.

<img src='/tutorial/notebooks/list_tiff_metadata/images/list_metadata.gif' />

### Export table

Select **output folder** location and click **export** in next cell.

<img src='/tutorial/notebooks/list_tiff_metadata/images/export_data.gif' />
