---
title: Display File Names vs Time Stamp
post: " <i class='fa fa-battery-full'></i>"
---

**Notebook name**: display_file_names_vs_time_stamp.ipynb

## Description

This notebook extracts the acquisition time and displays

 - time stamp vs file index
 - relative time stamp offset vs file index (offset between each file)
 - absolute time stamp offset vs file index (offset relative to first file loaded)

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Data Set

Select Images you want to check

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

Once you have selected your data, you will see a progress bar as the time stamp metadata are retrieved from the files.

### Display Time Stamp

The next cell will plot on the left side the **relative time offset** in seconds,
and on the right side, the **absolute time offset** in seconds.

**Relative time offset (s)**

This is the time between each image.

```
relative_time(i) = acquisition_time(image(i)) - acquisition_time(image(i-1))
```

**Absolute time offset (s)**

This is the time spent since we started to acquire the images. For the first image, this absolute time is 0 of course.

```
absolute_time(i) = acquisition_time(image(i)) - acquisition_time(image(0))
```

Here is the plot we got when using an acquisition time of 30ms
<img src='/tutorial/notebooks/display_file_names_vs_time_stamp/images/display_time_stamp.png' />

### List Files Loaded

The next cell display a list of all the fulle, relative and absolute time stamps.

<img src='/tutorial/notebooks/display_file_names_vs_time_stamp/images/list_time_stamps.gif' />