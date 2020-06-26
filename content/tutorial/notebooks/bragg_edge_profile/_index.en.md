---
title: Bragg Edge Profile 
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_profile.ipynb

## Description

This notebook has been implemented to produce an ASCII file of the **average counts** of the entire image, or of selected regions,
**versus lambda (Angstroms) and TOF (microS)**. 

The ASCII output file will look like this

<img src='/tutorial/notebooks/bragg_edge_profile/images/output_example.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## Step by step tutorial

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Data Folder

Select the **data folder** (usually normalized data via the [bragg_edge_normalization notebook]({{%relref "/tutorial/notebooks/bragg_edge_normalization/_index.md#activate-search" %}}))
 using the file selector. If the **time spectra** file is part of the folder, it will 
be automatically loaded, if **not**, you will have the option to select the **time spectra** file next. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/load_data.gif' />

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

The sample data will be automatically loaded.

## Calculate Bragg edge profile

### Define Experiment Setup

This is where you can set up your experiment and play with these values to make sure the Bragg Edges of the 
reference powder elements show up at the right lambda in your signal data. 

<img src='/tutorial/notebooks/bragg_edge_profile/images/experimental_setup.png' />

### Calculate signal of sample region

#### Select how many random files to use to select sample position

Define how many images, selected randomly, you want to use to figure out the position of the sample. Remember that
the more images you use, the longer it will take to display the ROI selection tool. The default value is usually
a good compromise but feel free to increase this number if you are unable to see your sample due to low statistics. 

#### Select the sample position

In order to calculate the Bragg edge signal of your sample, you must select the region of your sample in your images.
The same UI you used to select the background region will show up. Use the ROI tool to define one or more region overlapping 
your sample. 

### Calculate

This cell will calculate the Bragg edges data using the region selected.

### Display Bragg Edges vs Signal

This cell is optional and you need to run it only if you want to display the Counts vs lambda. 

<img src='/tutorial/notebooks/bragg_edge_profile/images/bragg_edges_vs_signal.png' />

Feel free to play with the **iPlot** widgets (above the plot) to zoom, pan, ... etc

### Export ASCII data

Select the output folder

<img src='/tutorial/notebooks/file_selector/images/select_output_folder.png' />

and then an ASCII file will be automatically created using the sample input folder as based name.

<img src='/tutorial/notebooks/bragg_edge_normalization_and_profile_extractor/images/output_file_message.png' />
