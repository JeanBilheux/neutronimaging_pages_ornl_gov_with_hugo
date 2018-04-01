---
title: Registration
post: " <i class='fa fa-battery-empty'></i>"
---

**Notebook name**: registration.ipynb

## Description

This notebook will allow the registration (alignment) of a set of images using a reference image of
your choice.

Here are the steps (**bold** for user input/manipulation)

 * **Select the stack of images**
 * launch application
 * Perform Auto alignment
 * and/or
 * Align images manually
 * use profile to help in the alignment and sliders to check images overlap

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select Images to Process

Select the images you want to process using the **File Selector**. Once you **click** the **Select** button, the time
stamp and the images will be automatically loaded. Wait for the progress bar to be done.

<img src='/tutorial/notebooks/water_intake_profile_calculator/images/select_files.gif' />

{{% notice info %}}
Need help using the [File Selector]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}})?
{{% /notice %}}

### Registration UI

<img src='/tutorial/notebooks/registration/images/description_of_ui.png' />

### Auto Registration

Let the program perform auto-registration of all the images selected using the default first image as a 
reference by clicking **Auto Registration**

<img src='/tutorial/notebooks/registration/images/auto_registration.gif' />

### Manual Registration

If you choose to manually align the images (except the reference image), click the **Manual Registration**
button. Then move manually the images selected using the **manual registration tool widgets**. 


<img src='/images/work_in_progress.png' />

