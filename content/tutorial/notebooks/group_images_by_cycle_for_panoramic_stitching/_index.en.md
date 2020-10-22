---
title: Group Images by Cycle for Panoramic Stitching
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: group_images_by_cycle_for_panoramic_stitching.ipynb

## Description

There are cases where several images have to be taken to cover the entire sample, as this one is going through changes.
To automate the acquisition, the system acquires the images going from one full cycle, full coverage of the sample, to
the next one without any changes in the location of the files, or even information in the name of the files. This notebook
will look at all the images of a given folder and will group them by cycle, then it will sort them in order to 
facilitate the work when stitching them together. This sorting can be something like working in rows first from left 
to right.

The following illustration shows this type of acquisition

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/3fullCycles.gif' />

**The goal being to go from a continuous list of files to a sorted list of cycles**

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/principle_of_notebook.png' />

## Tutorial

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the input folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder containing the data to work on.

The program will then automatically group the data by cycle using 2 PVs, data acquisition metadata, called **MotLiftTable**
and **MotLongAxis**. Those PVs record the vertical and horizontal position of the sample table. A simple change can
be done in the code to allow the program to use other, or more, PVs (contact [Jean Bilheux](/credits#jean_bilheux) to
learn more about this advanced feature).

The notebook will list the name of the input folder and the number of files, only TIFF, found in that folder.
Then on the left you will find the list of groups created. Just click on any of those groups to see the name
of the files that belong to the group and the corresponding metadata.

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/select_input_folder.png' />

### Sort files
 
Running the cell will allow you to select how your want to sort the files within each group/cycle.  

For example, if you define **MotLiftTable** as your first variable, the program will sort the files by their
**MotLiftTable** metadata, then will move to the second parameter to sort the files having an identical **MotLiftTable**.

The following sketches illustrates how this work when **ascending** is selected for both cases. Selecting **descending**
will reverse the images for that given PV. 

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/MotLiftAxis.png' />
<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/MotLongAxis.png' />
 
The bottom widgets allows you to browse through the groups and see how the files will be sorted and renamed.

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/sort_files.png' />
 
### Select the output folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the output location. 

The notebook will create a folder named based on the input folder name and then will create a folder for each group of
images.

<img src='/tutorial/notebooks/group_images_by_cycle_for_panoramic_stitching/images/output_files.gif' />
