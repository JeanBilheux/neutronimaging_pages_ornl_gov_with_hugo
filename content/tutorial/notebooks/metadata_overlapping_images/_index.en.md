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

When using **metadata**, you can display the current metadata as a string. But if you chose to, you can
also display a graph showing the current file metadata position over the entire set of images metadata.

#### Text

If you are working with a TIFF image, you will have the option of selecting one of the metadata available. Feel free
to change the label of this one if needed.
You can also define your own metadata by editing the table, or loading a file_vs_metadata file created by a notebook
specially dedicated to this purpose (WORK IN PROGRESS).

<img src='/tutorial/notebooks/metadata_overlapping_images/images/metadata_text.gif' />

{{% notice info %}}
It's sometimes necessary to format the default metadata value (especially if you want to display the graph). To do so,
right click in the right column of the table to reach the **metadata string parser (string filter)**.
<img src='/tutorial/notebooks/metadata_overlapping_images/images/string_filter_1.png' />
Then define the first and last part of the string to remove
<img src='/tutorial/notebooks/metadata_overlapping_images/images/string_filter_2.png' />
{{% /notice %}}

#### Graph

### Advanced feature

The **Advanced Table ...** button brings a new window that allows you to perform linear operation on various
metadata at the same time and display the result of this operation.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/ui_advanced.png' />

In order to define a new complex formula:
 
 * select a metadata to use via the top combo box
 * click **+** button to add it to the **math table**
 * change the coefficient in front of the new metadata if needed (default value is 1)
 * keep adding new metadata the same way
 
If a metadata needs to be removed from the equation, select the column and click **-**

Click **OK** to validate the equation and to return to main interface. 

The following animation demo how the advanced feature works.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/advanced_feature_demo.gif' />

### Export

**NB: Your application will look a little bit different from this animation**

You can now export all your images. The PNG files created will be a copy of the current UI image preview.

<img src='/tutorial/notebooks/metadata_overlapping_images/images/export.gif' />

<img src='/tutorial/notebooks/metadata_overlapping_images/images/exported_images.png' />
