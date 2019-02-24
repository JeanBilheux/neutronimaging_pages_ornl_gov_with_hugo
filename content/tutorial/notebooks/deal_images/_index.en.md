---
title: Deal Images
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: deal_images.ipynb

## Description

There will be cases where a folder contains several different experiment, or set up, or measure.
You will need to sort those images into their own folder. Hopefully this notebook can save you a
ton of time by doing it automatically. The algorithm to 'group' the images is based on the name of 
those files. 

The following picture illustrates the principle of the deal

<img src='/tutorial/notebooks/deal_images/images/deal_description.png' />

{{% notice warning %}}
This program assumes that the file names follow this schema  

```
text<image_ref>_<image_index>.<ext>
```

If it does not, run the notebook [rename_files.ipynb]({{%relref "/tutorial/notebooks/rename_files/_index.md" %}}).
{{% /notice %}}

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the Input Folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder that contains the images you need to separate.

### Select the Output Folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder that will contain the folders of all the deal images. 
