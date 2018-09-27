---
title: From Attenuation to Concentration
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: from_attenuation_to_concentration.ipynb

## Description

This notebook takes normalized data (attenuation) as input and will apply the formula defined to the data.
The data are then exported as TIFF. This formula convert attenuation into concentration values.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select data folder

Select the folder that contains the normalized images

<img src='/tutorial/notebooks/from_attenuation_to_concentration/images/load_data.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

### Define conversion formula

Define the conversion equation to use where

* A(x,Y) is the Attenuation (normalized) image
* H(x,y) is the concentration array that will be created

<img src='/tutorial/notebooks/from_attenuation_to_concentration/images/equation.png' />

### Converting data

Run this cell to convert the data. A progress bar will show you the evolution of the correction, then disapear once
it's done.

### Select output folder location

Select the location where the output folder will be created based on the name of the input folder

if input folder is **data_03**
output folder will be **data_03_concentration**

<img src='/tutorial/notebooks/from_attenuation_to_concentration/images/export_data.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

### Video showing entire process

<img src='/tutorial/notebooks/from_attenuation_to_concentration/images/full_example.gif' />
