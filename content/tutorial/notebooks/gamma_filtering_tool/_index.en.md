---
title: Gamma Filtering Tool
post: " <i class='fa fa-battery-full'></i>"
---

**Notebook name**: gamma_filtering_tool.ipynb

## Description

This notebook will allow you to compare data loaded without any correction against data loaded with gamma
filtering on. You will be able to change the gamma filtering coefficient to optimize the *cleaning of the gammas*
without dammaging the images.

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Images

Simply select all the images you want to work on.

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

### Display Images

<img src='/tutorial/notebooks/gamma_filtering_tool/images/starting_ui.png' />

#### Mouse Infos / Zoom and Pan

Moving the mouse over the **raw** or **filtered** image will give you its value in the status bar (bottom left) of the
UI. Also any **zoom** or **pan** transformation in one of the image will be reproduced in the other image.

<img src='/tutorial/notebooks/gamma_filtering_tool/images/zoom_pan.gif' />

#### Changing the filtering coefficient

After changing the **gamma filtering coefficient** and hitting **ENTER**, the entire stack of data will be reloaded
using the new filter coefficient. The table will show you the new percentage and number of pixels *cleaned*. The
**gamma filtered plot** will be refreshed to display the new cleaned selected image.

<img src='/tutorial/notebooks/gamma_filtering_tool/images/data_cleaned.gif' />

### Gamma Filtering Algorithm

If you wonder how the gamma filtering algorithm works and what is the meaning behind this magic **gamma filtering
coefficient**

Here is the workflow:

 * user determine the **gamma filtering coefficient** (coefficient). Value between 0 and 1.
 * Image per image, the program calculate the **average counts** (image_average_counts).
 * if the **coefficient * pixel_value > image_average_counts** then this pixel is considered to be a **gamma** and
is replaced by the **average value** of its 8 neighbor pixels.


{{% notice info %}}
Feel free to move the plot around and resize them!
<img src='/tutorial/notebooks/gamma_filtering_tool/images/resizing.gif' />
{{% /notice %}}