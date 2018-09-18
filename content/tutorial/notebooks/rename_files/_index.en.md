---
title: Rename Files
post: " <i class='fa fa-battery-empty'></i>"
---

**Notebook name**: rename_files.ipynb

## Description

This notebook allows you to rename a set of files. You can define

 * the prefix file name
 * the starting index
 * the index number of digits

### Main use of this notebook

In this notebook, we will correctly format the file name index of the file selected. This allows the sorting of the file name to works all the time. For example, there are many cases where the images are saved using the following convention

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



