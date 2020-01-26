---
title: Normalization with Simplify Selection
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: normalization_with_simplify_selection.ipynb

## Description

This notebook normalized the imaging data (tiff or fits) by removing the background and fixing the fluctuations of the
neutron beam. You will need:

 * select your sample images folder
 * Keep default option of using all open beam (OB) and dark field (DF) images from the same IPTS or select a different time frame
 * select output folder where the normalized images will be saved

The big improvement of this notebook compared to the old *normalization* notebook is that now, the notebook will take
care of finding all the OB and DF for you, and will match them to your sample data by making sure that:

 * the slits have the same position
 * the acquisition time is identical
 * the detector type is identical

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Selecting the Sample Images

Simply navigate to the folder containing all the data your want to normalize. The program will then list the
files with the most dominant extension, for example, if you have a folder with 10 tiff images and 2 fits, only the 10
tiff images will be used. All the sample images will be grouped according to the following criteria:

 * acquisition time
 * slits positions
 * detector type

The notebook will then retrieve all the OB and DF of the same IPTS by looking into the /raw/ob and /raw/df folders
respectively of your IPTS folder. The OB and DF that match the sample criteria will then be associated to their
sample data.

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/sample_ob_df_list_files.png' />

### Normalization workflow

This table will summarizes the data reduction that is about to take place. If a config has no OB, the table will let you
know that this config won't be normalized unless you provide at least one OB.  

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/recap.png' />
 
### Select Output Folder

Select the output location where you want all the normalized folders to be created. Then a message will let you know
when the normalization is done and the name of the files created.
 
{{% notice info %}}
Check the [folder selection tool tutorial]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})
to learn how to use the folder selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/output_message.png' />






