---
title: Images and Metadata Extrapolation Matcher
post: "<i class='fa fa-battery-quarter'></i> "
pre: "- "

---

**Notebook name**: images_and_metadata_extrapolation_parser.ipynb

## Description

There are cases where you need to define the **metadata value of a given image**. This is challenging when the file 
recording the metadata has no correlation with the images taken. This notebook will allow you to calculate, 
according to the time stamp of the image file, the metadata value. 

**This notebook takes 2 text files as input:**

- **filename vs timestamp text file** 
    * created by the notebook [create_list_of_file_name_vs_time_stamp.ipynb]({{%relref "/tutorial/notebooks/create_list_of_file_name_vs_time_stamp/_index.md#activate-search" %}})

- **metadata vs timestamp text file**
    * created by [metadata_ascii_parser]({{%relref "/tutorial/notebooks/metadata_ascii_parser/_index.md#activate-search" %}})
    
    or
    
    * created by [list_metadata_and_time_with_oncat]({{%relref "/tutorial/notebooks/list_metadata_and_time_with_oncat/_index.md#activate-search" %}})

Using those input files, the notebook will create a new text file of the file name and the corresponding metadata values you
previously selected. 

<img src='/tutorial/notebooks/images_and_metadata_extrapolation_matcher/images/output_ascii_file.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the file name vs time stamp text file

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
your metadata file. 

As specified in the notebook, this is the file you created using the notebook [create_list_of_file_name_vs_time_stamp.ipynb]({{%relref "/tutorial/notebooks/create_list_of_file_name_vs_time_stamp/_index.md#activate-search" %}})

This file looks like this

<img src='/tutorial/notebooks/images_and_metadata_extrapolation_matcher/images/filename_vs_timestamp.png' />

### Select the metadata vs time stamp text file

This file can be created using the notebook [metadata_ascii_parser]({{%relref "/tutorial/notebooks/metadata_ascii_parser/_index.md#activate-search" %}}) when the metadata have not been saved inside
the image file. 

or 

using the notebook [list_metadata_and_time_with_oncat]({{%relref "/tutorial/notebooks/list_metadata_and_time_with_oncat/_index.md#activate-search" %}}) when the metadata are inside the 
image file. Here is how to know if your file contains the metadata.