---
title: Metatadata Overlapping Images
post: "<i class='fa fa-battery-full'></i> "
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

## Profile UI Presentation

<img src='/tutorial/notebooks/metadata_overlapping_images/images/ui_presentation.png' />

## How Does it Work ?

### Scale

Select the **scale** option to add a dimension marker on top of the images. You can define:

 * orientation of the scale
 * size and label
 * color
 * thickness of the line
 * position of the scale/label in the image

<img src='/tutorial/notebooks/metadata_overlapping_images/images/scale.gif' />

### Metadata

When using **metadata**, you can either display the current metadata, or a graph showing the current file metadata
position.

#### Text

If you are working with a TIFF image, you will have the option of selecting one of the metadata available. Feel free
to change the label of this one if needed.
You can also define your own metadata by editing the table, or loading a file_vs_metadata file created by a notebook
specially dedicated to this purpose (WORK IN PROGRESS).

<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_text.gif' />

#### Graph

You can also display a graph showing the current metadata position related to the full metadata plot.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_graph.gif' />

### Export

You can now export all your images. The PNG files created will be a copy of the current UI image preview.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/export.gif' />

<img src='/tutorial/notebooks/metadata_overlapping_images/images/exported_images.png' />



