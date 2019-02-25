---
title: Fix Images
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: fix_images.ipynb

## description

This notebook allows you to fix a set of images by replacing all the pixels having the 
same value, by another value. For example, you can replace all the **Inf** values 
by **0** or **np.NaN**. 

Here is the list of things you can fix:

* Inf values
* NaN values
* Negative values

and here is the list of things you can replace with:

* np.NaN
* 0

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select your images

Using the [files selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), 
select the images you want to fix.

### Give statistics

In order to get an idea of what you need to correct, the next cell will display the following informations.

* **name** of the file
* **total number of pixels** in the image
* number and percentage of pixels with **negative values**
* number and percentage of pixels with **infinite (negative or positive) values**
* number and percentage of pixels with **non defined (NaN) values**

A slider allows you to check those parameters for each of the images you loaded.

<img src='/tutorial/notebooks/fix_images/images/statistics.png' />

### Display images and histograms

This is where you are able to visualize the corrections you are about to apply to the data. You can 
select which corrections you want to apply and see the effect on the image and its histogram.

You can slide thru the images to display

* the raw image (top left corner)
* the raw histogram (top right corner)
* the new corrected image (bottom left corner)
* the new histogram (bottom right corner)   

FIXME: Add a better example with bad data to correct

