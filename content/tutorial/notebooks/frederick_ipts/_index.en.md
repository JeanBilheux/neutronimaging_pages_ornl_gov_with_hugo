---
title: Frederick IPTS
post: " <i class='fa fa-battery-2'></i>"
---

**Notebook name**: frederick_ipts.ipynb

## Description

This notebook will re-group the data using the metadata recorded in the name of
the files.

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

<img src='/tutorial/notebooks/frederick_ipts/images/select_files.gif' />

### Sorting Files

Using the name of the files, the program will retrieve the Temperature (T) and
Pressure (P) of the data set.

Here is what those file names look like

<img src='/tutorial/notebooks/frederick_ipts/images/example_of_file_names.png' />

The program will then re-group the files by time stamp first and then by T and P
parameters.

This process may take some times as the program is loading all the data and calculating
the groups.

<img src='/tutorial/notebooks/frederick_ipts/images/select_files_process.png' />

### Display Images

By running the **display images** cell, a UI pops up that will allow you to
browse your data using the groups extracted from the previous step.

<img src='/tutorial/notebooks/frederick_ipts/images/preview_of_frederick_ui.gif' />

<img src='/images/morecomingsoon.png' />