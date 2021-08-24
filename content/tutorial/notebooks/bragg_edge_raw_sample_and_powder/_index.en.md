---
title: Bragg Edge Raw Sample and Powder
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: bragg_edge_raw_sample_and_powder.ipynb

## Description



## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select your IPTS

Check the full tutorial [here]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})</i>

### Select Raw Data Input Folder

Select the folder containing the full sample tof data. The program will automatically try to locate the time
spectra file in this folder. If not found, you will need to locate it next.

<img src='/tutorial/notebooks/bragg_edge_sample_and_powder/images/select_raw_data_input_folder.gif' />

### Select Open Beam Input Folder

Just like it was done for the sample data, select the open beam folder. The notebook will let you know if the **sample**
and **ob** folders have the same number of files. 

### Select ROI of sample 

You need to define the position of the sample in the view. 

#### Select how many random files to use to select sample position

The first widget allows you to select how many images to use
(those will be summed into a single view) to define that region of interest. The higher the number of images used, 
the longer the next user interface will take to show up. Usually the default value is a good compromise and is high
enough to get a good idea of the position of the sample.

#### Select location of sample in integrated image

Check the [ROI selection tool tutorial]({{%relref "/tutorial/notebooks/roi_selection_tool/_index.md#activate-search" %}})
to learn how to use that tool.

### Normalize Data

The program will use the **sample** and **ob** loaded to normalized the data. 

### Powder element

This is where you can define one, or more element to use to compare the Bragg edges with. 

You can choose any element from the following list:

'C (diamond)' 'C (graphite)' 'Si' 'Ge' 'AlAs' 'AlP' 'AlSb' 'GaP' 'GaAs'
    'GaSb' 'inconel' 'InP' 'InAs' 'InSb' 'MgO' 'SiC' 'CdS' 'CdSe' 'CdTe' 'ZnO'
    'ZnS' 'PbS' 'PbTe' 'BN' 'BP' 'CdS' 'ZnS' 'AlN' 'GaN' 'InN' 'LiF' 'LiCl'
    'LiBr' 'LiI' 'NaF' 'NaCl' 'NaBr' 'NaI' 'KF' 'KCl' 'KBr' 'KI' 'RbF' 'RbCl'
    'RbBr' 'RbI' 'CsF' 'CsCl' 'CsI' 'Al' 'Fe' 'Ni' 'Cu' 'Mo' 'Pd' 'Ag' 'W'
    'Pt' 'Au' 'Pb' 'TiN' 'ZrN' 'HfN' 'VN' 'CrN' 'NbN' 'TiC' 'ZrC0.97'
    'HfC0.99' 'VC0.97' 'NC0.99' 'TaC0.99' 'Cr3C2' 'WC' 'ScN' 'LiNbO3' 'KTaO3'
    'BaTiO3' 'SrTiO3' 'CaTiO3' 'PbTiO3' 'EuTiO3' 'SrVO3' 'CaVO3' 'BaMnO3'
    'CaMnO3' 'SrRuO3' 'YAlO3'
    
This is based on a library we developped called [BraggEdge](http://ornlneutronimaging.github.io/BraggEdge/demo.html#metadata-of-elements). 

To enter more than 1 element, use a colon to separate them. Run the next cell to check if the element is part of the
list.

<img src='/tutorial/notebooks/bragg_edge_sample_and_powder/images/list_of_elements.png' />

### Define Experiment Setup

Those information will be needed to convert the time of flight values into lambda.

### Calculate Bragg Edge Data

Just run this cell to let the notebook convert TOF information into lambda and prepare the data to compare them
with the unstrained, powder, Bragg edges.

### Display Bragg Edges vs Signal

Sample signal and unstrained Bragg edges of elements selected will be displayed on the same plot.

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/bragg_edges_vs_signal.png' />

Feel free to play with the **iPlot** widgets (above the plot) to zoom, pan, ... etc

<img src='/tutorial/notebooks/bragg_edge_signal_vs_powder_peaks/images/iplot_interaction.png' />
