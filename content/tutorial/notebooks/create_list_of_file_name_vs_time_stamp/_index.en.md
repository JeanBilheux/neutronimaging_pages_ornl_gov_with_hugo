---
title: Create List of Files of Names vs Time Stamp
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: create_list_of_file_name_vs_time_stamp.ipynb

## Description

This notebook extracts the acquisition time of the selected files and output an ascii file with the following
informations

 - full path of File name
 - time stamp (unix format)
 - time stamp (user format)
 - time offset (ms) relative to first image

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

### Select Output Folder

Simple, just navigate to the location where you want your ascii file written.

<img src='/tutorial/notebooks/create_list_of_file_name_vs_time_stamp/images/output_folder.png' />

### Output Folder Created

The Ascii file created will look like this

```
#filename, timestamp(s), timestamp_user_format, timeoffset(s)
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0001.tiff, 1532610101.2023919, 2018-07-26 09:01:41, 0.0
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0002.tiff, 1532610101.2320013, 2018-07-26 09:01:41, 0.02960944175720215
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0003.tiff, 1532610101.261922, 2018-07-26 09:01:41, 0.059530019760131836
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0004.tiff, 1532610101.2918322, 2018-07-26 09:01:41, 0.08944034576416016
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0005.tiff, 1532610101.32187, 2018-07-26 09:01:41, 0.11947822570800781
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0006.tiff, 1532610101.352108, 2018-07-26 09:01:41, 0.14971613883972168
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0007.tiff, 1532610101.3818908, 2018-07-26 09:01:41, 0.17949891090393066
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0008.tiff, 1532610101.411917, 2018-07-26 09:01:41, 0.20952510833740234
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0009.tiff, 1532610101.4418778, 2018-07-26 09:01:41, 0.2394859790802002
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0010.tiff, 1532610101.4718854, 2018-07-26 09:01:41, 0.26949357986450195
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0011.tiff, 1532610101.5023768, 2018-07-26 09:01:41, 0.2999849319458008
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0012.tiff, 1532610101.531988, 2018-07-26 09:01:41, 0.32959604263305664
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0013.tiff, 1532610101.5619035, 2018-07-26 09:01:41, 0.3595116138458252
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0014.tiff, 1532610101.59197, 2018-07-26 09:01:41, 0.38957810401916504
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0015.tiff, 1532610101.6220326, 2018-07-26 09:01:41, 0.41964077949523926
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0016.tiff, 1532610101.6519294, 2018-07-26 09:01:41, 0.4495375156402588
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0017.tiff, 1532610101.6820183, 2018-07-26 09:01:41, 0.4796264171600342
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0018.tiff, 1532610101.7119684, 2018-07-26 09:01:41, 0.5095765590667725
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0019.tiff, 1532610101.7419527, 2018-07-26 09:01:41, 0.5395607948303223
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0020.tiff, 1532610101.7720513, 2018-07-26 09:01:41, 0.5696594715118408
/Volumes/my_book_thunderbolt_duo/IPTS/IPTS-21115/Huggies_3cm_thick/20180726_Huggies_3cm_0000_0021.tiff, 1532610101.802108, 2018-07-26 09:01:41, 0.5997161865234375
...
```

