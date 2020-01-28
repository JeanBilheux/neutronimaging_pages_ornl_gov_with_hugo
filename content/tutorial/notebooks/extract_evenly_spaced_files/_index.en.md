---
title: Extract Evenly Spaced Files
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: extract_evenly_spaced_files.ipynb

## Description

This notebook allows you to copy into a new folder (extract) 1 every n files from the source folder. You
will need to provide the **skipping** factor **n** in the notebook.

**Example:**

let's pretend you selected a folder (*/Users/j35/my_data/*) containing the following 21 images

**Input**

 * image001.fits      
 * image002.fits
 * image003.fits
 * image004.fits
 * image005.fits
 * image006.fits
 * image007.fits
 * image008.fits
 * image009.fits
 * image010.fits      
 * image011.fits
 * image012.fits
 * image013.fits
 * image014.fits
 * image015.fits
 * image016.fits
 * image017.fits
 * image018.fits
 * image019.fits
 * image020.fits
 * image021.fits

and you decided to extract **1 every 5 files** in the **Desktop**. 

The notebook will create the folder called */Users/j35/Desktop/my_data_1_every_5_files* and will copy the following
files there

 * image001.fits      
 * image006.fits
 * image011.fits
 * image016.fits
 * image021.fits

## How does the notebook work?

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the folder containing the images to extract

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder

### Extraction coefficient

Select the number of images you want to skip. The notebook will give you live the list of files that will then be
extracted.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/extraction_method.png' />

### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the combine images.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/select_output_folder.png' />

### Extracting

Once the output folder has been selected, the files will be automatically extracted (copied) into the output folder.
Then a message will let you know when the process is done and where you can find the files copied.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/result_of_notebook.png' />


