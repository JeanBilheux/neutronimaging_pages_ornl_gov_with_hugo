---
title: Bragg Edge - Signal vs Powder Peaks
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_signal_vs_powder_peaks.ipynb

## Description

The main goal of this notebook is to display the ideal Bragg Edges of a list of elements and compare their signature
to the signal of a set of FITS (MCP data) taken. Experimental set up can be changed by:

- distance source - detector
- detector time offset

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Working Folder

Select the **working folder** using the file selector. If the **time spectra** file is part of the folder, it will 
be automatically loaded, if **not**, you will have the option to select the **time spectra** file next. 

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/load_data.gif' />

{{% notice info %}}
Check the [file selection tool tutorial]({{%relref "/tutorial/notebooks/file_selector/_index.md#folder_navigation" %}})
to learn how to use the file selector tool.
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />
{{% /notice %}}

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

### Display Bragg Edges vs Signal

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/bragg_edges_vs_signal.png' />

Feel free to play with the **iPlot** widgets (above the plot) to zoom, pan, ... etc

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/iplot_interaction.png' />
