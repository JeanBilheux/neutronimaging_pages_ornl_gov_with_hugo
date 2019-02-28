---
title: From .dsc Time Info to ASCII File vs Time
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: from_dsc_time_info_to_ascii_file_vs_time.ipynb

## Description

There are cases where you will need to use the metadata from the **dsc** file to retrieve the time information as
the files themselves do not have this information any more (because they are not the original images anymore, because 
they have been moved, ...).

So this notebook will use the **dsc** files and match the time stamp information they contain with the base file name.
Then will create an ascii file of the equivalent TIFF image vs time stamp

**INPUT**

*folder containing .dsc files*

**OUTPUT**

filename_vs_timestamp.txt
```
sample_0000.tif 1045454545  
sample_0001.tif 1045454546
sample_0002.tfi 1045454547
```

## Instructions

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the DSC Folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder that contains the **.dsc** files.

### Select the Image Folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder that contains the **images** (TIFF or FITS) to match with the **dsc** files.

### Select the Output Folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder where the ascii file listing the image files and their time stamp will be created.

### Ascii File Created

Once you have selected the output folder, the ascii file will be automatically created and will look something like this

<img src='/tutorial/notebooks/from_dsc_time_info_to_ascii_file_vs_time/images/??.png' />

