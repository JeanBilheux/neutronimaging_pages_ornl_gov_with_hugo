---
title: Normalization
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: normalization.ipynb

## Description

This notebook normalized the imaging data (tiff or fits) by removing the background and fixing the fluctuations of the
neutron beam. You will need:

 * select your images
 * select your open beam (OB)
 * optional - select the dark field (DF)
 * optional - select one or more background region in your sample images
 * run the normalization
 * select output folder where the normalized images will be saved

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### loading the Images

You need to provide the list of **samples**, **OB** and **DF** (if needed). To do so, just **SHIFT + ENTER** the
following cell to display a *selection tool wizard*.

<img src='/tutorial/notebooks/normalization/images/loading_images_1.gif' />

The dialogbox will start listing the files from the IPTS folder you selected in the first cell. Feel free to navigate
to find your data set.

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

* Select your **sample images**
* click **Next Step>>**
* Select your **OB images**
* click **Next Step>>**
* **OPTIONAL** Select your **DF images**
* click **Next Step>>** to let the program load all your images.

<img src='/tutorial/notebooks/normalization/images/loading_images_2.gif' />

### Select Background Region

**SHIFT + ENTER** to run the cell. A new User Interface (UI) will come to life. If you can not see the UI, check
behind the notebook window.

{{% notice info %}}
In order to speed up the display of the data, the notebook randomly select **5%** of the stack of sample image 
selected. If you want to change that coefficient, edit the **config.py** file found in the *__code* folder and change
the variable value called **percentage_of_images_to_use_for_roi_selection**.
<img src='/tutorial/notebooks/normalization/images/config.png' />
{{% /notice %}}

<img src='/tutorial/notebooks/normalization/images/roi_selection_1.gif' />

Just click **OK** if you do not want to select any region of interest (ROI).

If you want to provide one, or more, ROI, click **+** on the
right of the GUI and move/resize the ROI using the mouse, or the table values.

<img src='/tutorial/notebooks/normalization/images/roi_selection_2.gif' />

### Normalization

This cell runs the normalization and let you know the progress of the calculation via a progress bar.

<img src='/tutorial/notebooks/normalization/images/normalization.png' />

### Export

Select where you want to output the normalized data, then run the following cell. Once the output folder selected,
a folder name after the input data folder is created and will contain all the normalized data.

<img src='/tutorial/notebooks/normalization/images/export.png' />


