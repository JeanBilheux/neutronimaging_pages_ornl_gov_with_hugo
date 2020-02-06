---
title: Rename Files
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: rename_files.ipynb

## Description

This notebook allows you to rename a set of files. You can define

 * the prefix file name from scratch or used part of the old name
 * the starting index
 * the index number of digits

### Main use of this notebook

In this notebook, we will correctly format the file name index of the file selected. 
This allows the sorting of the file name to works all the time. For example, there are many cases where the 
images are saved using the following convention.

**Wrong filename index**

```
image_1.tif
image_2.tif
image_3.tif
image_4.tif
...
image_10.tif
image_11.tif
...
image_100.tif
```

Using this convention, any sorting algorithm will sort them as followed

**Wrong sorting**
```
image_1.tif
image_10.tif
image_100.tif
...
```

So this notebook will fix this issue by renaming the files

**correct filename index**

```
image_001.tif
image_002.tif
image_003.tif
image_004.tif
...
image_010.tif
image_011.tif
...
image_100.tif
```

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select images to rename

Using the file dialog tool, select the folder for which you want to renmame the files.

**Only the  most dominant file type (ex: tiff, fits) from the folder will be renamed**

<img src='/tutorial/notebooks/rename_files/images/select_folder.gif' />

### Define new naming schema

#### Current schema name

This is where you define the way the current file name is defined. You need to specify what string separates the first 
part of the file name with the index. If you decide to not fully rename the images, the string before this **separator** 
will be kept in the new file name.

The **Random input** dropdown list displays a random selection of the input files, to help you in defining the
**separator** string. Play with it to make sure you correctly defined the current file name (what is prefix, what is a
separator). Use the slider to the right of the **file name prefix** to define the prefix part of the name (as shown in
the following animation). 

<img src='/tutorial/notebooks/rename_files/images/playing_with_slider.gif' />

#### New naming schema

Here, you define if you want to keep the old prefix or not, the new **prefix** file name, **index separator**,
 **number of digits** and **offset** of this index.

_Example:_

 * **old file name**:   experiment_0845454_10.tiff
 * **separator**: _
 * **new file name prefix**: my_image
 * **number of digits**: 4
 * **offset**: 15
 * **new file name will be**: my_image_0025.tiff

<img src='/tutorial/notebooks/rename_files/images/new_file_name.gif' />

#### Result

The bottom part of the cell will show the result of the naming on the first image selected.

If the new name shows an **Error**, checks your **pre index separator**.

### Output folder

You simply need to select where the new renamed file will be created. Then the program will copy the selected files
and renamed them in the folder you selected.

<img src='/tutorial/notebooks/rename_files/images/output_result.gif' />

Feel free to check the dropdown list that shows the old name versus the new name of each file.