---
title: Extract Evenly Spaced Files
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: extract_evenly_spaced_files.ipynb

## Description

This notebook allows you to copy into a new folder (extract) 1 every n files from the source folder. You
will need to provide the **skipping** factor **n** in the notebook. A new feature of the notebook allows you to 
review the files to extract and manually replace or remove them from the final process. You will also have the 
option to rename those files, as they are copied, in order to keep a linear increasing index starting at index 0.

**Example:**

let's pretend you selected a folder (*/Users/j35/my_data/*) containing the following 21 images

**Input**

 * image_001.fits      
 * image_002.fits
 * image_003.fits
 * image_004.fits
 * image_005.fits
 * image_006.fits
 * image_007.fits
 * image_008.fits
 * image_009.fits
 * image_010.fits      
 * image_011.fits
 * image_012.fits
 * image_013.fits
 * image_014.fits
 * image_015.fits
 * image_016.fits
 * image_017.fits
 * image_018.fits
 * image_019.fits
 * image_020.fits
 * image_021.fits

and you decided to extract **1 every 5 files** in the **Desktop**. 

The notebook will create the folder called */Users/j35/Desktop/my_data_1_every_5_files* and will copy the following
files there

 * image_001.fits      
 * image_006.fits
 * image_011.fits
 * image_016.fits
 * image_021.fits

or if you decide to rename them

 * image_0000.fits      
 * image_0001.fits
 * image_0002.fits
 * image_0003.fits
 * image_0004.fits

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

### Manual review of selected files

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/interface_1.png' />
<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/interface_2.png' />

This interface gives a preview of the file selected and give a change to the user to **remove** or **replace** any
of the image with any of the neighbor files. 

The bottom part of the user interface display the **mean square error** of two consecutive images. Algorithm can
be found [here](https://www.pyimagesearch.com/2014/09/15/python-compare-two-images/). By default, the 
**max threshold** is equal to the maximum mean square error. Moving the threshold around will highlight in the 
list of files widget the images that are outside the new threshold.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/moving_threshold_around.gif' />

#### Remove or Replace files

Right click in the list of files widget to either **remove** the selected file, or **to access a new user 
interface** that will allow you to replace the selected image with any neighbor image not already part of the selection.

 * **Remove** selected file
 
 Right click on the file you want to remove and click **remove**
 
<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/remove_file.gif' />
 
 * **Replace with** selected file
 
 Right click on the file you want **to replace**. In the new UI, select any of the file listed in the widget
 on the right of the UI. The list of files is determined using the initial list of files "surrounding" the current
 selected file, but that are not already in the list of files to extract.
 
<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/replace_with_file.gif' />
 
### Rename or not Files

This is where you have the option to rename of not the output files.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/rename_files.gif' />

### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the combine images.

<img src='/tutorial/notebooks/file_selector/images/select_output_folder.png' />

### Extracting

Once the output folder has been selected, the files will be automatically extracted (copied) into the output folder.
Then a message will let you know when the process is done and where you can find the files copied.

<img src='/tutorial/notebooks/extract_evenly_spaced_files/images/result_of_notebook.png' />
