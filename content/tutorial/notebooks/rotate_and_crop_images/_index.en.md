---
title: Rotate and Crop Images
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: rotate_and_crop_images.ipynb

## Description

You will use this notebook if you need to **crop** and/or **rotate** a set of images.

The application will ask you to select the images (FITS or TIFF) you want to modify. 
Then a User Interface (UI) will allow you to define the cropping region as well as the rotation 
angle to apply to the images. 
You will be able to browse through the images to check the result and then create the transformed
images before exporting them to a new output folder as TIFF images.

<img src='/tutorial/notebooks/rotate_and_crop_images/images/demo_ui.gif' />


## How it Works

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select your Images

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the images you want to work with.

Once selected, your images will be automatically loaded. 

### Crop and/or Rotate your Images

This is where you will apply the correction to your images. 

<img src='/tutorial/notebooks/rotate_and_crop_images/images/ui_description.png' />

#### How to crop the images:
 
 * **move the box** around by **clicking one of the edge** and **without releasing the mouse** move the box to the new location
 * **resize the box** by **clicking** the **bottom right corner** and **dragging** it to the new size. 
 
#### How to rotate the images:

  Simply by entering the **angle** value in the text field. The angle is using the geometrical convention, with counter clock wise
  rotation direction.
  
#### Apply changes to all images:

   By clicking the **apply on all images** button, you will apply those correction to all images and **quit this UI** 
   
#### Export Images

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select
where you want the output images to be created. 

The program will automatically create a folder based on the rotation angle you defined

For example:

 A folder named **rotated_0.5deg** is created when the angle is 0.5 degrees.
