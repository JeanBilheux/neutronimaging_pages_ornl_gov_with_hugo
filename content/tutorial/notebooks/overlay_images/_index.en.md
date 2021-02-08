---
title: Overlay Images
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: overlay_images.ipynb

## Description

This notebook will overlay (merged) two folders of images taken with different resolution. The low resolution, wide
angle, images will be scaled in order to fit the high resolution. The high resolution can be placed inside the low
resolution images automatically or manually.

<img src='/tutorial/notebooks/overlay_images/images/preview_of_application.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Images

#### High resolution images

Select the folder that contains all the high resolution images you want to use.

{{% notice info %}}
Check this tutorial if you need help using the 
[file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})
{{% /notice %}}

Move on to the next cell to select the low resolution images.

#### Low resolution images

Repeat the process for the low resolution images. Make sure the two folders have the same number of images

### Launching the interface

The next cell will bring the main UI to life. 

<img src='/tutorial/notebooks/overlay_images/images/preview_of_ui.png' />

{{% notice info %}}
Use the splitters to resize any of the windows.
<img src='/tutorial/notebooks/overlay_images/images/resizing.gif' />
{{% /notice %}}

**The first tab will allows you:**
 
  * to roughly rescale the low resolution images to fit the pixel size of the high
resolution images
  * place the high resolution images at the right place inside the low resolution images

#### Step 1

Using the <span style="color: red">RED</span> and <span style="color: blue">BLUE</span> markers.
The goal being to place the <span style="color: red">RED</span> markers at the corresponding spot in the **high 
resolution** image and the **low resolution** image. Repeat it for the <span style="color: blue">BLUE</span> markers.

Make sure you use the mouse to facilitate the selection by **Zooming (wheel)** or **panning (left and drag click)**.

<img src='/tutorial/notebooks/overlay_images/images/auto_align.gif' />

#### Step 2

<img src='/tutorial/notebooks/overlay_images/images/step2_preview.png' />

The second step allows you to improve the alignment of the selected high resolution image and apply that changes 
(**scaling factor**, **xoffset** and **yoffset**) to all the other images. 

A couple of tools are available to help you position the images, the **profiler** and  **transparency** tools.

<h4><span style="color: red"> Manual scaling, xoffset and yoffset</span></h4>

It's possible to manually define the **scaling factor**, the **xoffset**, and the **yoffset** position of the 
currently selected high and low resolution images. Just enter the new value and hit **ENTER** to validate the new
value. You can also manually move the high resolution image by 1 or 5 pixels either way using the **-, - -, +** and 
**+ +** buttons. 

As soon as the **scaling factor, xoffset** and **yoffset** values differ from the values calculated by the automatic 
mode, the **overlay mode** in the table of list of files will display <span style="color: blue">Manual</span>.

<img src='/tutorial/notebooks/overlay_images/images/manual_overlay.gif' />

<h4><span style="color: red">Profiler tool</span></h4>

Turn on the **profiler tool** to get a live profile plot of the vertical and horizontal **high resolution** and **low resolution** profiles
around the cursor position. This will help overlaying the two images.

<img src='/tutorial/notebooks/overlay_images/images/profiler.gif' />

<h4><span style="color: red">Transparency</span></h4>
  
Using the transparency feature allows to see "through" the high resolution image, the low resolution to help the
overlay. 

<img src='/tutorial/notebooks/overlay_images/images/transparency.gif' />

{{% notice warning %}}
Once you are satisfied with the overlay of the "working" images, click the **Manually overlay all images** in order
to apply that settings to all the images. Once all the images have been overlaid, the **export overlaid images** button
becomes available.
<img src='/tutorial/notebooks/overlay_images/images/manually_overlaid_all_images.gif' />
{{% /notice %}}

### Export the final images

Click the **Export overlaid images** button to export the overlaid images. Each TIFF image created will have a few
of new metadata infos:

 * **scaling factor**
 * **xoffset**
 * **yoffset** 
 
<img src='/tutorial/notebooks/overlay_images/images/metadata_list.png' />
 