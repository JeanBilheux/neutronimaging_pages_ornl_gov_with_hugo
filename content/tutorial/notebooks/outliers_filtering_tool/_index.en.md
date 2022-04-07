---
title: Outliers Filtering Tool
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: outliers_filtering_tool.ipynb

## Description

This notebook allows you to compare data loaded without any correction against data loaded with outliers
removed. Outliers pixels are:

* **dead pixels** (pixels with 0 counts)
* **gamma counts** (pixels with very high counts compare to neighbor pixels)

If any of the **dead pixels** and/or **gamma counts** options is turned on, a **bad** pixel is replaced by the median 
value of the surrounding pixels. This *surrounding* region can be defined by the user, and is by default a square of \
3 by 3 pixels around the pixel of interest.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Images

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

### Launch the User Interface (UI)

Run the next cell to launch the UI
<img src='/tutorial/notebooks/outliers_filtering_tool/images/load_and_display_images.png' />
<img src='/tutorial/notebooks/outliers_filtering_tool/images/ui.png' />

### Display Images

{{% notice warning %}}
In some cases, the first image you see of your sample is zoom out too much. 
click the **Auto** scale to reset the display.
<img src='/tutorial/notebooks/outliers_filtering_tool/images/auto_scale.gif' />
{{% /notice %}}

<img src='/tutorial/notebooks/outliers_filtering_tool/images/starting_ui.png' />

#### Mouse Infos / Zoom and Pan

Moving the mouse over the **raw** or **filtered** image will give you its value in the status bar (bottom left) of the
UI. Also any **zoom** or **pan** transformation in one of the image will be reproduced in the other image.

<img src='/tutorial/notebooks/outliers_filtering_tool/images/zoom_pan.gif' />

#### Filtering Options

##### Dead Pixels

When turned on, all pixels with 0 counts will be replaced by the median value of the block surrounding that pixel.
The block width and height is defined by the **radius** widget at the bottom right of the interface (Median filter options)

##### High Intensity Counts

A pixel is considered to have a "high intensity counts" if the following formula is true

 counts_of_pixel_in_raw_image * coefficient > counts_of_pixels_in_median_image
 
where the coefficient is a value between 0 and 1.

##### Median Filter Options

This defines the region surrounding the pixel to calculate the median value. 

ex: if the pixel have the following values [1, 1, 2, 3, 4, 4, 5, 6], the median is *3.5* ((3+4)/2)
ex: [1,2,3,4,5,5,6,6,8], median is *5*

{{% notice info %}}
Feel free to move the plot around and resize them!
<img src='/tutorial/notebooks/outliers_filtering_tool/images/resizing.gif' />
{{% /notice %}}

### Histogram of Raw and Filtered Data Sets

You can visualize the histogram before after filtering by clicking the **Histogram** view.

<img src='/tutorial/notebooks/outliers_filtering_tool/images/histogram.png' />

### Table

Only the data of interest are loaded when requested. If one clicks a row, the data of this raw are loaded and go
through the filtering process. Statistics about the pixels cleaned is then displayed in the table

## Export 

Click the **Correct All Images...** button (bottom right) to correct all the data and create a new folder based on the
**input folder name + _outlisers_corrected**. 

{{% notice info %}}
If the output folder already exists, the current date and time will be prefixed to the folder name to make sure
the previous folder is not replaced!
{{% /notice %}}
