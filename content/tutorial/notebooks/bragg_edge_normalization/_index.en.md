---
title: Bragg Edge Normalization
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_normalization.ipynb

## Description

This notebook has been implemented to produce an ASCII file of the average counts of the entire image, or of selected regions,
versus lambda (Angstroms) and TOF (microS). 

It's also possible to compare the signal with the Bragg edge signature of a given unstrained powder.

Output will look like this

<img src='/tutorial/notebooks/bragg_edge_normalization/images/output_example.png' />



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

Just like you did for the sample data, select the folder containing the open beam (OB) data.

### Selection of Sample in the Image

In order to calculate the signal of the loaded images, you must define the location of your sample in the image. But
before doing so, the program will need to load a random subset of those images. You will need to define how many images 
you want to use to select that sample. A subset has been defined for you by default. Using this value (N), the program
will load N images randomly choosen within the list of images in the working folder.

**Remember** The more images you want to load, the longer it will take. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/how_many_images.png' />

Once this subset has been defined, running the next cell will bring a user interface that will allow you
to define the location(s) of your sample. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/select_sample_roi.gif' />

### Select Powder Elements

It's now time to select the **powder elements** for which you want to see the **Bragg Edges** on top of your
signal.

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/si_element.png' />

### Define Experiment Setup

This is where you can set up your experiment and play with these values to make sure the Bragg Edges of the 
reference powder elements show up at the right lambda in your signal data. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/experimental_setup.png' />

### Calculate Bragg Edges Data

This cell will calculate the Bragg edges data using the region selected, if any.

### Display Bragg Edges vs Signal

This cell is optional and you need to run it only if you want to display the Counts vs lambda. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/bragg_edges_vs_signal.png' />

Feel free to play with the **iPlot** widgets (above the plot) to zoom, pan, ... etc

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/iplot_interaction.png' />

### Export ASCII data

Select the output folder

<img src='/tutorial/notebooks/file_selector/images/select_output_folder.png' />

and then an ASCII file will be automatically created using the sample input folder as based name.

<img src='/tutorial/notebooks/bragg_edge_normalization/images/output_file_message.png' />
