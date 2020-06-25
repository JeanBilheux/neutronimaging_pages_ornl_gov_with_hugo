---
title: Bragg Edge Normalization and Profile Extractor 
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_normalization_and_profile_extractor.ipynb

## Description

This notebook has been implemented to:
 * normalized the TOF data
 * produce an ASCII file of the average counts of the entire image, or of selected regions,
versus lambda (Angstroms) and TOF (microS). 

The ASCII output file will look like this

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/output_example.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Sample Folder

Select the **sample folder** using the file selector. If the **time spectra** file is part of the folder, it will 
be automatically loaded, if **not**, you will have the option to select the **time spectra** file next. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/load_data.gif' />

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

The sample data will be automatically loaded.

### Select OB Folder

Just like you did for the sample data, select the folder containing the open beam (OB) data. Once you selected this
folder the data will be automatically loaded.

### Selection of background region in the image

You have the option to define a region of your image that **is background** for sure. This will improve the normalization.

To do so, you first need to specify how many random images you want to use to help the selection. The more images
you select, the higher resolution your image will have but the longer it will take to display it. Usually the 
default number of images provided is a good compromise. If you can not see your sample in the image, just close the UI and 
increase the number of images to use.

Once the **ROI selection tool UI** show up, you can select, or not, 1 or more regions. You need to make sure that/those 
region(s) is/are away from the sample. If the sample covers the entire image, do not select any region!
 Once you are done, **click OK** to close the UI.

**Remember** The more images you want to load, the longer it will take. 

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/how_many_images.png' />

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/select_sample_roi.gif' />

### Perform normalization

Just run this cell to run the normalization algorithm. 

### Export normalized data

Select where you want to export all the normalized images. You have the option to create a folder if needed. 

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/export_normalized_images.gif' />

## Calculate Bragg edge profile

### Define Experiment Setup

This is where you can set up your experiment and play with these values to make sure the Bragg Edges of the 
reference powder elements show up at the right lambda in your signal data. 

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/experimental_setup.png' />

### Define the position of your sample

In order to calculate the Bragg edge signal of your sample, you must select the region of your sample in your images.
The same UI you used to select the background region will show up. Use the ROI tool to define one or more region overlapping 
your sample. 

### Calculate signal of sample region

This cell will calculate the Bragg edges data using the region selected.

### Display Bragg Edges vs Signal

This cell is optional and you need to run it only if you want to display the Counts vs lambda. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/bragg_edges_vs_signal.png' />

Feel free to play with the **iPlot** widgets (above the plot) to zoom, pan, ... etc

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/iplot_interaction.png' />

### Export ASCII data

Select the output folder

<img src='/tutorial/notebooks/file_selector/images/select_output_folder.png' />

and then an ASCII file will be automatically created using the sample input folder as based name.

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/output_file_message.png' />
