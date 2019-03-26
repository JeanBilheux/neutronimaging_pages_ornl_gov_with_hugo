---
title: List Metadata and Time with ONCat
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: list_metadata_and_time_with_oncat.ipynb

## Description

Using the ORNL Database service [ONCat](https://oncat.ornl.gov/#/) in the back, users can create an ASCII file 
with the acquisition time and metadata of interest selected. The output file will look like this

<img src='/tutorial/notebooks/list_metadata_and_time_with_oncat/images/preview_of_ascii_file.png' />

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

### Log in to ONCat

In order to be able to retrieve the metadata from our database (ONCat) you will need to log in by typing your XCAMS
password, then hit ENTER.
A message will show you if you entered the right password or not. 

<img src='/tutorial/notebooks/list_metadata_and_time_with_oncat/images/loginoncat.gif' />

### Select Metadata to Keep

The notebook will list all the metadata found in the first image you selected with an example of values, again found
in the first file. Select all the metadata you want to see in the final ASCII output file. Use **CTRL + CLICK** to 
select more than one metadata. 

<img src='/tutorial/notebooks/list_metadata_and_time_with_oncat/images/select_metadata.gif' />

### Create and Export ASCII File

It's now time to select your output folder. 

{{% notice info %}}
Need help using the [Folder Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

The program will automatically name the file based on the input folder

**For example:**

 * **input folder**: 20180814
 
 * **ASCII file**: 20180814_metadata_report.txt
 
 
 
 