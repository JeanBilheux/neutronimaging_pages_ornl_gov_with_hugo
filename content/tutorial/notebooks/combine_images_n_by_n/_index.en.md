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
 
{{% notice info %}}
Not seeing the algorithm you want to use? Please let me know and I will add it (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)
{{% /notice %}}
 
**Example:**

let's pretend you selected a folder containing the following 21 images

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

and you decided to combine the first **4** images, then the following 4, and so on

<img src='/tutorial/notebooks/combine_images_n_by_n/images/how_to_combine_images.png' />

This will produce 5 files 

 * 4_files_combined_0001.tif
 * 4_files_combined_0002.tif
 * 4_files_combined_0003.tif
 * 4_files_combined_0004.tif
 * 4_files_combined_0005.tif
 
where the first one will be the combination of image001.fits, image002.fits, image003.fits and image004.fits

**NB:** Because there were 21 images to start with, the last image was dropped (image021.fits) as 21 can not be evenly
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

### Select output location

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the location where you want to create the combine images.

### Merging

Once you have entered the output folder, the images will be automatically merged and a progress bar will let you
know of the progress of the operation. Then finally, the notebook will let you know when it's done and show you where 
those files have been created. 

<img src='/tutorial/notebooks/combine_images_n_by_n/images/output_files.gif' />




