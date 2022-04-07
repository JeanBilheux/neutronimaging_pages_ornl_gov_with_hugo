---
title: Normalization with Simplify Selection
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: normalization_with_simplify_selection.ipynb

## Description

This notebook normalized the imaging data (tiff or fits) by removing the background and fixing the fluctuations of the
neutron beam. You will need to follow these steps:

 * select your sample images folder
 * Select the OB from the list proposed 
 * select output folder where the normalized images will be saved

The big improvement of this notebook compared to the old *normalization* notebook is that now, the notebook takes
care of finding all the OB and DF for you, and matches them with your sample data by making sure that:

 * the slits have the same position
 * the acquisition time is identical
 * the detector type is identical

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Selecting the Sample Images

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/selection_of_data.gif' />

Simply navigate to the folder containing all the data your want to normalize. The program will then list the
files with the most dominant extension, for example, if you have a folder with 10 tiff images and 2 fits, only the 10
tiff images will be used. All the sample images will be grouped according to the following criteria:

 * acquisition time
 * slits positions
 * detector type

The notebook will then retrieve all the OB and DF of the same IPTS by looking into the **/raw/ob** and **/raw/df** folders
respectively of your IPTS folder. The OB and DF that match the sample criteria will then be associated to their
sample data.

At that point, **you have the power** to finalize the selection:

 * For each configuration, you can reject it from normalization by **turning off** the switch named **Normalize this 
configuration**

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/turn_off_normalization.png' />

 * The list of OB proposed include **ALL** the OBs found with matching metadata (see above) in the corresponding IPTS,
no matter how long before or after they were acquired. By default they are all selected in the list widget. Feel free
to narrow down that selection by manually selecting them (see next animation).

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/manual_selection_of_obs.gif' />

 * You can also narrow down that selection by setting up yourself a time range before and after the sample data runs 
 (see the next animation)

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/custom_time_range.gif' />

 * According to the number of sample and open beams loaded, you may have the option to combine the open beams or not,
 and to provide the algorithm to use to combine them.
 
 *Here are the possible scenario:*
  
 * there is as many **sample** and **ob** data. You can either **combine** the **OBs** or not. If you choose not
    to combine them, each sample will use 1 OB.
 
 * the number of **sample** and **ob** is different, you don't have the choice to combine or not, but you can select 
    how the **OBs** will be combine, either **median** and **mean**.

 A table at the bottom of the cell will summarize the state of that normalization. 
 
<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/how_to_combine.png' />

### ROI selection

In order to improve the normalization, you have the option to select a region of interest (ROI). This ROI must be
a region of background only in your sample image. The algorithm will then use the difference of intensity in the
background of the sample and the same region in the open beam to get a coefficient that will be apply to the normalization.  

To do so, click the **Selection of region of interest (ROI) - OPTIONAL** button. Use the user interface that just
popped up to make your selection, or just close it if you changed your mind. 

{{% notice info %}}
If you need help using the ROI selection tool, [check this tutorial]({{%relref "/tutorial/notebooks/roi_selection_tool/_index.md#activate-search" %}})
{{% /notice %}}

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/roi_selection.gif' />

### Normalization workflow

This table will summarizes the data reduction that is about to take place. If a config has no OB, the table will let you
know that this config won't be normalized unless you provide at least one OB. Also, if you decided to turn off the
normalization of any particular config, you will see it in that table.

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/recap2.png' />
 
### Select Output Folder

Select the output location where you want all the normalized folders to be created. Then a message will let you know
when the normalization is done and the name of the files created.
 
{{% notice info %}}
Check the [folder selection tool tutorial]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})
to learn how to use the folder selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

<img src='/tutorial/notebooks/normalization_with_simplify_selection/images/output_message.png' />

{{% notice info %}}
If the output folder already exists, the current date and time will be prefixed to the folder name to make sure
the previous folder is not replaced!
{{% /notice %}}
