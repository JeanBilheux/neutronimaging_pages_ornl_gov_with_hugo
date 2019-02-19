---
title: Bin Images
post: " <i class='fa fa-battery-full'></i>"
pre: "- "
---

**Notebook name**: bin_images.ipynb

## Description

This notebook rebin a image, or set of images. That means the pixels will be
group according to the rebin parameter you will select. 

For example, if you select a rebin value of 2, pixels will be group 2x2 (see images 
as an illustration of such a rebin) and those pixels will be averaged. 

In the following example, we start with an image of 8 by 8 pixels. Please note the
value of each pixels (number of counts). 

<img src='/tutorial/notebooks/bin_images/images/original_image.png' />
<center>fig 1: original 8 by 8 image.</center>

Then we selected a **rebin** value of 2.

<img src='/tutorial/notebooks/bin_images/images/images_mean_2_binning.png' />
<center>fig 2: Rebin by 2 for a final image size of 4 by 4.</center>

{{% notice info %}}
In the case where the width and/or height of the image can not be evenly divided by the 
rebin coefficient, the last uncompleted bin will be removed from the final image.
<img src='/tutorial/notebooks/bin_images/images/truncated_image_after_rebin.png' />
{{% /notice %}}

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the images to rebin

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the images you want to rebin.

NB: After selection of the images, those will be automatically loaded in memory.

### Select Bin Parameter

It's time to select your **bin parameter**. The cell will also gives you, for 
information, the size of your image before and after rebin.

<img src='/tutorial/notebooks/bin_images/images/bin_parameter_selection.png' />

### Select Output Folder

Just one more step. Select where you want those new images to be created. 
Once selected using the [folder selection tool](({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}),
the images will be automatically rebin and exported. The program will create a folder called after the input folder
from where the initial images were retrieved inside the output folder you selected following this convention

 * **Input folder**: my_data
 * **Output folder**: my_data_rebin_by_2   (or whatever the rebin coefficient you selected)