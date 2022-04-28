---
title: Group Images by Cycle for Grating Experiment
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: group_images_by_cycle_for_grating_experiment.ipynb

## Description

Grating experiment in CT mode collect a multitude of data files, all created in the same folder. Those data must be 
sorted using first the **rotation** value and then the **G0** value. Then

The following notebook will automatically sort the data by group using two metadata. By default those are the **G0** and 
**rotation** angle, but any other metadata found in the tiff file can be used. Once sorted, the files are renamed to
be processed by Angel and the configuration file, excel file, used by Angel is generated to speed up the input
required by the user.

## Tutorial

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select data to sort

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder containing the data to process, and then select all the images to work with. The selection of files instead 
of the entire data in the folder, allows you to have *sample* and *ob* within the same folder without compromising
the sorting. 

### Select Metadata to use for sorting

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/select_metadata.png' />

This is where you can specify how the images will be sorted. The left column will be used as the **outer loop** parameter
and the right column the **inner loop** parameter. A Search tool is available at the top to allow you to quickly narrow 
down the list by entering a few keystrokes. The button labeled **X** to the right of the search fields reset the
search criteria. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/search_demo.gif' />

### Grouping

Using the list of files you defined, and the metadata criteria, the files are sorted and the resulting grouping 
is displayed when running this cell. 

The left column displays the name of the group, i.e., the outer loop. The second column, the original name of the images
and just to its right, the new name that will be used. 

{{% notice info %}}
In the case where more than 1 image have the same inner and outer metadadata values, the images are then combined
using a **median** algorithm.
{{% /notice %}}

In the far right column is displayed the corresponding metadata values of the image selected.

Under the table a label reminds the user of the folder name where these images are coming from.

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/grouping.png' />

### Select Output Folder

Select where you want the new images to be created. Once selected, the notebook will automatically trigger the 
**renaming** and **grouping** of those files. A couple of progress bars will allow you to follow the progress of the 
process. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/select_output_progress_bars.gif' />

### Generate Angel Configuration File (Excel)

This step is optional but will surely simplify your life if you need to normalize the data using Angel. 

The first cell (%gui qt) is necessary to bring to life the user interface in the next cell.

Running the second cell will give you a few options

 1. did you sort the **sample** or the **ob** data?
 This is required to be able to populate the right columns in the excel document
 
 2. do you want to create a **new excel** document or do you want to **load a previously created excel**?
 
#### Create new Excel

If you select this option, a new excel will be created and the **sample** or **ob** columns will be filled with the
files from this notebook. Default values for all the other fields are provided. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/new_excel_presentation.gif' />

Any cell in <html><span style="color:red">red</span></html> is an indication that this excel will not work in 
Angel in the current state. 

**Editing the table**

You can manually edit all the cells, except the *rotation* column. Once the cell has been edited, click the **button**
below the table labeled **Checking if current table can be loaded in Angel** to check the status of the excel document.

Once you modified any of the widget found inside the cell, a pop up window asks you **if you want to duplicate that change
to all the other widgets of the same column, or not**. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/duplicate_changes.png' />

**Right clicking inside the table**

Some of the cells, such as the one requesting a file or a folder, allows you, by **right clicking** inside the cell
to bring a file dialog. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_grating_experiment/images/browsing_for_file_demo.gif' />

You can either
 
  * browse for a file and replace the content of the current cell
  * browse for a file and replace the content of all the cells of this column 

A right click inside any of the cell also allows you to **remove the current row** or to **duplicate that row to the
bottom of the table**.

**Save as ...**

Click that button, placed at the bottom right of the user interface, to export that table into an excel document.

{{% notice info %}}
Some of the cells can not be modified, such as all the cells in the the **rotation** column.
The last 3 columns, **sample_information**, **used_environment** and **osc_pixel** are not used in Angel.
{{% /notice %}}

#### Open existing excel

In this case, a file dialog will ask you to select the excel file to use and will bring the same user interface. 
Refer to the section **Create new excel** to learn how the UI works. 
