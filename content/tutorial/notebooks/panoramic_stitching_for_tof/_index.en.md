---
title: Panoramic Stitching for TOF 
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: panoramic_stitching_for_tof.ipynb

## Description

This notebook stitches images acquired in TOF mode. 

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/panoramic_stitching_for_tof_preview.png' />

The notebook takes a set of folders as input. Each folder corresponds to a different coverage of the sample and contains
all the TOF images acquired using the MCP detector. You will need to manually position either the integrated signal over
all the TOF, or the best contrast image (calculated using the Dual energy algorithm described in the notebook 
[dual energy]({{%relref "/tutorial/notebooks/dual_energy/_index.md#activate-search" %}})). Then the program will stitch
every single tof image using those same parameters. At the end you will have a folder of the stitch images with as
many images as any of the input folder.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Folders to Process

Using the **folder selector tool**, select all the folders you want to work on. Each folder must contain the TIFF images
of a single panoramic stitching (all the images of that folder will be stitched together). 

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/select_folders.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## How Does it Work ?

This UI has been designed to automatically stitch all the images of the various TOF/lambda after manually stitch
the integrated or best contrast images.

## Step by Step Tutorial

### Step 1 - Select with which image you want to work

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/tab1_preview.png' />

The first tab **Calculate best contrast images** allows you to determine the images with the best contrast. 2 options 
are offered:

 * Integrated image
 * Best contrast image
 
The **Integrated images** are for each folder selected the sum of all the images. The **best contrast image** uses
the algorithm defined in the [dual energy notebook]({{%relref "/tutorial/notebooks/dual_energy/_index.md#activate-search" %}})).
Feel free to play with the binning size to improve the contrast. Once you are happy with the image mode you
selected, just move on to the next tab **Coarse alignment**.

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/step1.gif' />

### Step 2 - Coarse Alignment

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/tab2_preview.png' />

Because the images produced in TOF mode do not have the position of the motor as metadata, it's up to you to
roughly determine their position using the table. Just select all the images, and only one time, and position
them relative to each other. Once you are happy with your selection, click the **Validate Coarse Alignment** button
to record those positions. You can now move on to the next and final step.

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/step2_coarse_alignment.gif' />


### Step 3 - Fine Alignment

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/tab3_preview.png' />

The top left corner image, first image/file from the list, is fixed. This is the reason why selecting the first raw
in the table will display a **blue border** around the image. 

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/reference_image.png' />

Any other row selected will display a **red border** around the image selected. You have three options to move those
images. 

 * using the mouse
 * using manual offset button to jump by 1 or 5 pixels at a time
 * entering offset values directly in the table

**Using the Mouse**

To activate the mouse mode, **click** the **From -> To pointer** switch at the top of the UI. This will brings a 
couple of target labels FROM and TO within the panoramic view. Simply move the FROM target within the image selected
region, inside the red box, to a feature you recognized in the previous image stitched. Move the TO target to that
same feature and then click **Move image of active ro FROM -> TO** to reposition that image. 

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/from_to_mode.gif' />

{{% notice warning %}}
the **Move image of active row FROM ->TO** button will be enabled only when the **FROM target** is within the image
selected (surrounded by a red border).  
<img src='/tutorial/notebooks/panoramic_stitching/images/FROM_within_selected_image.gif' />
{{% /notice %}}

{{% notice tip %}}
The UI provides an horizontal and vertical profiler tool to help in the alignment of 2 images. 
<img src='/tutorial/notebooks/panoramic_stitching/images/profiler.png' />
Feel free to move around the horizontal and vertical profilers, resize them in length or width as illustrated here.
<img src='/tutorial/notebooks/panoramic_stitching/images/profile_resize_move.gif' />
The **BLACK** plot shows the profile from the reference image, the **RED** plot shows the profile of the working image.
{{% /notice %}}

**Using manual offset buttons**

Using those buttons, you can move the working image by **1** or **5**pixels at a time horizontally or vertically.
<img src='/tutorial/notebooks/panoramic_stitching/images/manual_move_buttons.png' />

**Using table**

You can also directly entered the xoffset or yoffset of any image, except the first one, within the table. Double 
click the field you want to edit to change the x or y offset. 

<img src='/tutorial/notebooks/panoramic_stitching_for_tof/images/manual_move.gif' />


#### Export panoramic images

You can now repeat the alignment on all the TOF slices by clicking the **Export Panoramic Images** button. 
You will need to select the output folder where you want to create the final folder which will be named
after the parent input folders name. 

{{% notice info %}}
For the region of overlap between two images, the notebook simply takes the average of the two images as illustrated here.
<img src='/tutorial/notebooks/panoramic_stitching/images/math_of_overlap.png' />
{{% /notice %}}
