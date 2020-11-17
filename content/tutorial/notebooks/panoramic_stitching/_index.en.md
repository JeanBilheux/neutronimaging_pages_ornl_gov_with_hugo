---
title: Panoramic Stitching
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: panoramic_stitching.ipynb

## Description

The main goal of this notebook is to stitch a set of images as shown here.

<img src='/tutorial/notebooks/panoramic_stitching/images/panoramic_result.png' />

This notebook takes a set of folders as input, such as the one created by the 
[group_images_by_cycle_for_panoramic_stitching]({{%relref "/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/_index.md#activate-search" %}}).
You need to manually stitch the images of one of those folders and then the notebook will apply the same settings to
all the other folders by matching motor_position/pixel_offset.

By default this notebook is defined to look for the 2 motor parameters called **MotLiftTable.RBV** and **MotLongAxis.RBV**. 
(contact [Jean Bilheux](/credits#jean_bilheux) to customize the notebook to other motor names).

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

<img src='/tutorial/notebooks/panoramic_stitching/images/select_folders.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## Interface Presentation

<img src='/tutorial/notebooks/panoramic_stitching/images/ui_preview.png' />

## How Does it Work ?

Ths UI has been designed to help you stitch all the images of the first, by default, folder selected. Once this is
done, you will click the **Automatic stitch all other folders using those parameters** button to stitch all the
other folders/images. Then you can export the panoramic images created as TIFF.

### Step by Step

#### Step 1 - stitch one group of images (any of them will work)

The top left corner image, first image/file from the list, is fixed. This is the reason why selecting the first raw
in the table will display a **blue border** around the image. 

<img src='/tutorial/notebooks/panoramic_stitching/images/first_image_selected.png' />

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

<img src='/tutorial/notebooks/panoramic_stitching/images/mouse_stitch_image.gif' />

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
<img src='/tutorial/notebooks/panoramic_stitching/images/manual_xoffset_and_yoffset_in_table.gif' />

#### Step 2 - Repeat settings defined on all other folders

Once you have completely aligned all first images of the current folders, you can repeat the settings on all
the other folders by clicking the **Automatically stitch all other folders using those offset parameters** button. The
program will calculate for each image the coefficient x and y offset versus motor position and then will apply that
coefficient on the new images. This rule of 3 allows a perfect horizontal and vertical positions of the images.
Once it's done, simply browse through the folders to check the alignment of all the images. 

#### Step 3 - Create all panoramic images

You need first to select the output location where the image will be created. A folder will be created based on the name
of the parent directory of the input folders.  

For the region of overlap between two images, the notebook simply takes the average of the two images as illustrated here.
<img src='/tutorial/notebooks/panoramic_stitching/images/math_of_overlap.png' />





