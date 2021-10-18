---
title: Metadata Overlapping Images
post: "<i class='fa fa-battery-full'></i> "
pre: "- "
---

**Notebook name**: metadata_overlapping_images.ipynb

## Description

This notebook allows you to add a dimension scale to your images. You can also add a given metadata value
for each of the images, or a graph showing the entire metadata plot and the current image metadata position on this graph.

* Scale added on top of image
<img src='/tutorial/notebooks/metadata_overlapping_images/images/scale.png'>

* Metadata of current image
<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_text.png'>

* Graph of all metadata and current metadata value
<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_graph.png'>

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Images

Select the images you want to process using the **File Selector**. Once you **click** the **Select** button, the time
stamp and the images will be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/calibrated_transmission/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

{{% notice info %}}
A progress bar will show you the loading progress. Make sure you wait for the busy signal to goes away before moving
on to the next cell.
<img src='/tutorial/notebooks/metadata_overlapping_images/images/progress_bar.gif' />
{{% /notice %}}

## Profile UI Presentation

<img src='/tutorial/notebooks/metadata_overlapping_images/images/ui_presentation.png' />

## How Does it Work ?

### Scale

<img src='/tutorial/notebooks/metadata_overlapping_images/images/scale_ui.png' />


Select the **scale** option to add a dimension marker on top of the images. You can define:

 * orientation of the scale
 * size and label
 * color
 * thickness of the line
 * position of the scale/label in the image

<img src='/tutorial/notebooks/metadata_overlapping_images/images/scale.gif' />

### Metadata

When using **metadata**, two features are offered:
 * you can display and personalize 1 or 2 metadata values on top of the plot
 * you can also plot a metadata versus file index, or versus another metadata
 
We are going to review each of those features one by one as they each come up with many settings to you define.

#### Displaying metadata in image

<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_text_demo.gif' />

If you want to display on each image 1 or 2 metadata values, use this feature. **RIGHT CLICK** inside the table and 
click **Select Metadata ...**. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/right_click.png' />

This will bring the **Select Metadata Toolbox**. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/select_metadata_toolbox.png' />

Select first the metadata you want to use. Some of the metadata only have a value, others have a string attached
to the value. You can either use the metadata as it is, or if you want to remove part of the string, use the 
**String cleaning** widgets to remove some text. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/string_cleaning.gif' />

If the metadata, before or after cleaning, can be converted to a float, you have access to widgets that allow you
to perform up to 2 linear operations on it. If any equation has been defined, this equation will be applied to this metadata
for every single file selected and will be displayed in the final table once you click SELECT. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/linear_operation.gif' />

##### Settings

<img src='/tutorial/notebooks/metadata_overlapping_images/images/settings_metadata_1.png' />

In order to customize the text, you can:
 * move it inside the image
 * change the size of the font
 * add a string BEFORE (prefix) and/or AFTER (suffix)

<img src='/tutorial/notebooks/metadata_overlapping_images/images/settings_metadata_1.gif' />

#### Plot metadata in image

This plot is used to see the value of the current file metadata over the entire stack of images selected. For 
example, in the case of a sample where the Temperature changes over time, this plot will show the current 
temperature of the image as well as the temperature of all the images. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/plot_data_demo.gif' />

It's possible to change the default x-axis (file index) to any of the 2 metadata. RIGHT CLICK and click 
X-AXIS or Y-AXIS. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/change_x_y_axis.gif' />

You can define the legend of each axis using the settings widgets. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/plot_graph_legend.png' />

### Export Table

You can export the table into an ascii file. Click **Export Table ...** and select the output folder. 

<img src='/tutorial/notebooks/metadata_overlapping_images/images/export_table.png' />

### Export

You can now export all your images. The PNG files created will be a copy of the current UI image preview. Click
**Export Images ...** at the bottom right and select the location where you want to create the images.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/exported_images.png' />
