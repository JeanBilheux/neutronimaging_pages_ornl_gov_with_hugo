---
title: Extract NeXus DASlogs
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: extract_nexus_daslogs.ipynb

## Description

Some experiments required saving some metadata such as a furnace temperature over time in order to match each image file
with the proper metadata. This notebook allows you to select 2 axis of metadata to retrieve. Usually time and value of that
metadata. 

For example, this tutorial will use the PV (name of DAS variable) called **BL3_SE_ND1:CH2:PV** which is in fact the 
temperature of a furnace. One will select the **time** array and then the **data** array. The notebook will then extract those 
information and will also format the time axis as follow:

- relative time, default time recorded in the NeXus,
- absolute time, using relative time + starting time of NeXus
- global relative time. This is in the case you selected more than 1 NeXus, the global relative time will use the time the
first NeXus was started as reference, or time t=0s

The notebook will then create an output ASCII file named after the metatdata selected that will look like this

<img src='/tutorial/notebooks/extract_nexus_daslogs/images/example_output_file.png' />



## How does the notebook work?

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the NeXus

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select all 
the NeXus you want to retrieve metadata from.

### Select the Metadata to extract

Using the first NeXus selected the notebook displays the list of metadata found in the DASlogs entry. Make you way
through the tree to select your x and y-axis. 

The notebook offers the possibility to interpolate the data by defining the interpolation step to use. The algorithm
will then use a linear interpolation using the 
[scipy splrep method](https://docs.scipy.org/doc/scipy/reference/generated/scipy.interpolate.splrep.html).

### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the ASCII file

<img src='/tutorial/notebooks/file_selector/images/select_output_folder.png' />

### Full Demo

<img src='/tutorial/notebooks/extract_nexus_daslogs/images/extract_das_logs_full_sequence.gif' />



