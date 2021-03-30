---
title: MCP Chips Corrector
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: mcp_chips_corrector.ipynb

## Description

This notebook will allow you to correct individual MCP chips by applying an offset as shown here.

<img src='/tutorial/notebooks/mcp_chips_corrector/images/before_after.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Folders to Process

Using the **folder selector tool**, select the folder you want to work on. This folder must contain the entire FITS
images to correct. All the FITS images, except the SummedImg, will be corrected. 

<img src='/tutorial/notebooks/panoramic_stitching/images/select_folders.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

## Interface Presentation

<img src='/tutorial/notebooks/mcp_chips_corrector/images/ui_preview_1.png' />
<img src='/tutorial/notebooks/mcp_chips_corrector/images/ui_preview_2.png' />

## How Does it Work ?

The first tab **Setup** allows to define the chips that needs to be corrected. The image displayed is the integrated
signal of all the images selected. A profile region, that can be
resized and reoriented, allows to calculate automatically the average counts on either side of a chip gap. The
difference of average counts leads to the calculation of a corrector coefficient that is applied to the
working chips (red framing around it). The second tab **with correction** displays the resulting correction applied
to the integrated image. 

### Step by Step

#### Step 1 - Select the profile to use

In this first step, you need to define a region, either vertically or horizontally, that overlap the working
chip and another chip to estimate the correction to apply. If the profile selected is horizontally for example, the 
program will integrate all the pixels in the vertical direction within the profile region. The profile is then
displayed on the right side of the UI with the average counts for either side of the gap, gap highlighted as a 
green vertical line. 

<img src='/tutorial/notebooks/mcp_chips_corrector/images/profile.gif' />

The profile region can be resized using the 2 handles as shown here.

<img src='/tutorial/notebooks/mcp_chips_corrector/images/profile_handles.gif' />

#### Step 2 - Select working chip and position profile

Using bottom widgets, select the chip you want to correct. The **working** chip will be highlighted by a red
contour in the display window. Then move, and resize if needed, the profile to make sure it covers either the 
**working** chip and another chip to use as reference counts. Ideally, try to profile a common feature on either 
side of the chip gap. 

<img src='/tutorial/notebooks/mcp_chips_corrector/images/bad_and_good_profiles.png' />

#### Step 3 - Visualize correction and repeat correction on all images

Jump to the second tab called **with correction** to visualize the correction on the integrated image. 

 * If correction seems to work, click bottom switch to select output folder where all the images will be corrected.
 * if correction still seems to be off, you can define a manual correction value in the bottom right widget. 
 
<img src='/tutorial/notebooks/mcp_chips_corrector/images/export.gif' />
