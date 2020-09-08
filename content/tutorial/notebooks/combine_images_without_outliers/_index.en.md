---
title: Combine Images without Outliers
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: combine_images_without_outliers.ipynb

## Description

The goal of this notebooks is to combine images (mean) after removing, for each pixel, the pixel with the min and max 
counts.

The main purpose is to improve the statistics of the images by removing pixel with very low or very high counts
such as the "gamma" pixels. This is the reason why a minimum of 3 images minimum needs to be provided for each position
to combine. 

But in order to let the program figure out how to combine the images together from the full stack you selected, the 
notebook will list all the images found in the folder you selected and will let you choose the first images to combine 
together. The program will then determine the part of the name that does not change between those images and then 
automatically use it on all the other images of the folder to find out how to combine the entire set. 

Due to a limitation of unix, make sure the last digit of the file name has enough digit to cover the entire stack. This 
is because unix treats image called **image2** as being after **image12**. For this purpose, use the 
[renamed notebook]({{%relref "/tutorial/notebooks/rename_files/_index.md#activate-search" %}})

so for example, let's pretend the first few images are 
<img src='/tutorial/notebooks/combine_images_without_outliers/images/example_list_of_raw.png' />

And if you select the first 4 images 
<img src='/tutorial/notebooks/combine_images_without_outliers/images/example_list_of_combine.png' />

The images will then be combined by looking at the part of the string that does not change **20200821_Femur_0010_000_000**

## Tutorial

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select how you want to combine the first images

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder containing the data to combine. 

The program will then display all the files found in the folder and will ask you to select how you want to combine the
first images. As explained in the introduction, the algorithm will then determine the fix part of the names between
those files to learn how to combine the rest of the stack of images. Select at least 3 images!

The notebook will then display how the new output files will be named and their corresponding initial images combined.

<img src='/tutorial/notebooks/combine_images_without_outliers/images/selection_of_images.gif' />

### Select output folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the output location. 

The notebook will create a folder named based on the input folder name and will show you the progress of the conversion 
via a progress bar. 
