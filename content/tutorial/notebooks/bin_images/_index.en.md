---
title: Rebin Images
post: " <i class='fa fa-battery-quarter'></i>"
pre: "- "
---

**Notebook name**: bin_images.ipynb

## Description

This notebook rebin a image, or set of images. That means the pixels will be
group according to the rebin parameter you will select. 

For example, if you select a rebin value of 2, pixels will be group 2x2 (see images 
as an illustration of such a rebin). 

In the current state, 2 types of rebin can be selected, **add** or **mean** value of 
the pixels (see images)

In the following example, we start with an image of 8 by 8 pixels. Please note the
value of each pixels (number of counts). 

<img src='/tutorial/notebooks/bin_images/images/original_image.png' />
<center>fig 1: original 8 by 8 image.</center>

Then we selected a **rebin** value of 2.

<img src='/tutorial/notebooks/bin_images/images/images_mean_2_binning.png' />
<center>fig 2: Rebin 2 with a mean algorithm.</center>

<img src='/tutorial/notebooks/bin_images/images/images_sum_2_binning.png' />
<center>fig 3: Rebin 2 with a sum algorithm.</center>

{{% notice info %}}
In the case where the width and/or height of the image can not be evenly divided by the 
rebin coefficient, the last uncompleted bin will be removed from the final image.
<img src='/tutorial/notebooks/bin_images/images/truncated_image_after_rebin.png' />
{{% /notice %}}


