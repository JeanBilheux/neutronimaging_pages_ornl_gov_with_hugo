---
title: Combine Images Sequentially using the Metadata Information
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: sequential_combine_images_using_metadata.ipynb

## Description

This notebook was implemented to automatically combine runs according to any of the metadata you select. 

In other words, let's pretend you take 10 images at a given sample position, move the sample then take another 10 images,
until the end of the cycle. The algorithm will look at the metadata value you selected, in this case 2 motor positions,
and if they match within a given range (1 by  default), the images are considered to be of the same sample at the same place. 
They will be combined. If one of the metadata is outside the error range, or if the name of the run changed, then this is considered
to be a different run or/and different location. 

The notebook will create a dictionary of run # ->  position# -> list of files. This then wll be used to combine the images using 1 of
3 different algorithms (check the following notebook to learn more about those algorithms [combine_images]({{%relref "/tutorial/notebooks/combine_images/_index.md#activate-search" %}}))

## Tutorial

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the Input Folders

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folders containing the images you want to work on.

### select metadata to match

Using the first file of the folder selected, the notebook will display the list of metadata (and their value) to 
let you select which metadata we need to check to decide if the new file needs to be combine to the previous one or not.

By default, 2 metadata are selected

* MotLiftTable.RBV
* MtLongAxis.RBV

<img src='/tutorial/notebooks/sequential_combine_images_using_metadata/images/list_metadata.png' />

### How do you want to combine the folders

What algorithm do you want to use to combine them. You have the option to **add** or to **mean** (arithmetic mean or
geometric mean) those images.

<img src='/tutorial/notebooks/sequential_combine_images_using_metadata/images/how_to_combine.png' />

{{% notice info %}}
Not seeing the algorithm you want to use? Please let me know and I will add it (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)
{{% /notice %}}

### Create and Checking Merging List 

The program will load the data, in order to retrieve the metadata, and will create the list that will be used in the
final step to merge the data. If anything seems wrong during this step, contact me (<a href="/en/credits#jean_bilheux">Jean Bilheux</a>)

<img src='/tutorial/notebooks/sequential_combine_images_using_metadata/images/check_merging_list.gif' />

### Select output folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the output location.

A double progress bar (folder and file progress) will show you the progress of the combination of the folders. 

<img src='/tutorial/notebooks/sequential_combine_images_using_metadata/images/output_files.gif' />

<img src='/tutorial/notebooks/sequential_combine_images_using_metadata/images/final_message.png' />


