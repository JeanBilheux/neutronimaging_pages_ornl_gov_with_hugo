---
title: Combine Images n by n
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: combine_images_n_by_n.ipynb

## Description

This notebook allows you to combine the images contain in the folder you selected by group of n by n using 3 different algorithms.

 * Arithmetic Mean
 
<img src='/tutorial/notebooks/combine_images_n_by_n/images/arithmetic_mean.png' />
 
 * Geometric Mean

<img src='/tutorial/notebooks/combine_images_n_by_n/images/geometric_mean.png' />

 * Add
 
 * Median
 
{{% notice info %}}
Not seeing the algorithm you want to use? Please let me know and I will add it (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)
{{% /notice %}}
 
**Example:**

let's pretend you selected a folder containing the following 21 images

**Input**

 * data_000_010_000.fits      
 * data_000_010_001.fits
 * data_000_010_002.fits
 * data_000_010_003.fits
 * data_000_020_004.fits
 * data_000_020_005.fits
 * data_000_020_006.fits
 * data_000_020_007.fits
 * data_000_030_008.fits
 * data_000_030_009.fits      
 * data_000_030_010.fits
 * data_000_030_011.fits
 * data_000_040_012.fits
 * data_000_040_013.fits
 * data_000_040_014.fits
 * data_000_040_015.fits
 * data_000_050_016.fits
 * data_000_050_017.fits
 * data_000_050_018.fits
 * data_000_050_019.fits
 * data_000_060_020.fits

and you decided to combine the first **4** images, then the following 4, and so on

<img src='/tutorial/notebooks/combine_images_n_by_n/images/how_to_combine_images.png' />

This will produce 5 files, for which you will have the option to named based on their initial file name, or not.

**Option 1** using their base name

 * data_000_010_000.tif
 * data_000_020_001.tif
 * data_000_030_002.tif
 * data_000_040_003.tif
 * data_000_050_004.tif
 
 or **Option 2**, using new names
 
 * image_000.tif
 * image_001.tif
 * image_002.tif
 * image_003.tif
 * image_004.tif
 
where the first one will be the combination of data_000_010_000.fits, data_000_010_001.fits, data_000_010_002.fits and data_000_010_003.fits

**NB:** Because there were 21 images to start with, the last image was dropped (data_000_060_020.fits) as 21 can not be evenly
divided by 4!

## How does the notebook work?

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the folder containing the images to merge/combine

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder

### Merging method

It's time to select your merging algorithm (check the description at the top of this web page for
the explanation of the algorithms). 

<img src='/tutorial/notebooks/combine_images_n_by_n/images/merging_methods.png' />

### How do you want to combine those images

This is where you specify how you want to combine them. If you select **2**, the first 2 images will be combined, then 
the next 2, and so on. 
If the number of images can not be evenly divided by this coefficient, then the last images won't be used.

<img src='/tutorial/notebooks/combine_images_n_by_n/images/how_to_combine_images.png' />

### Preview of how the files will be combined and renamed 

This is where you can check that the files are correctly grouped. You can also choose to rename the new files or
use the base file name of the input data sets. In this case the program will conserve the common string of the file name
up to the previous "_" (underscore) file separator. 

* For example if the two following files are combined

 - /Volumes/G-DRIVE/IPTS/IPTS-12345/CT/20210505_1C30_150_tomo_0010_002_000_015.tif
 - /Volumes/G-DRIVE/IPTS/IPTS-12345/CT/20210505_1C30_150_tomo_0010_002_000_016.tif

the resulting base name of the output file will look like

- 20210505_1C30_150_tomo_0010_002_000.001.tif

<img src='/tutorial/notebooks/combine_images_n_by_n/images/preview_result.gif' />
 
### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the combine images.

### Merging

Once you have entered the output folder, the images will be automatically merged and a progress bar will let you
know of the progress of the operation. Then finally, the notebook will let you know when it's done and show you where 
those files have been created. 

<img src='/tutorial/notebooks/combine_images_n_by_n/images/output_files.gif' />

### Working with TOF data

 If you are working with TOF data set, where a **_Spectra.txt** file is present, the notebook will automatically create
a new **_Spectra.txt** file according to the merging parameters you selected. 
  
  * The first column of the file, *time*, will be the average of the corresponding row/files combined
  * The second column, *total counts* will use the same algorithm than the one you selected in the notebook.

<img src='/tutorial/notebooks/combine_images_n_by_n/images/time_spectra_creating_explanation.png' />

If a Spectra file has been located and a new one created, the full file path of that file will be displayed in the 
notebook

<img src='/tutorial/notebooks/combine_images_n_by_n/images/output_in_tof_mode.png' />

{{% notice info %}}
If the output folder already exists, the current date and time will be prefixed to the folder name to make sure
the previous folder is not replaced!
{{% /notice %}}

