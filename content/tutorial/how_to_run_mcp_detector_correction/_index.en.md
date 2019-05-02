---
title: MCP Det. Corr.
weight: 700
pre: "<b>5.7 </b>"
---

The following tutorial will guide, step by step, in running the MCP correction program

<img src='/tutorial/how_to_run_mcp_detector_correction/images/parent_folder_selected.PNG' /> 

### Description

Every single data acquired using the MCP detector needs to be corrected for detector efficiency. 

**Old Way**

In the past, one had to go through the following steps:
    
 * start the windows command line tool
 * locate the .exe script (using file browser) and drag and drop it into the command line window
 * add a space in the command line 
 * locate the first image of the data set to correct
 * Run the script and wait ...
 * rename the folder *correction* created by the script
 * grab this folder and move it to final location
 * **repeat** for all other set of data

**New Way**

 * start **MCPcorrection** program
 * select root folder containing all data set 
 * select output folder
 * click **correction** button

{{% notice info %}}
The **parent folder** must be the folder seating on top of the data folder! 
This looks confusing? 
Well just follow the following diagram. In such a case, you should select the first folder!
<img src='/tutorial/how_to_run_mcp_detector_correction/images/folder_structure.png' /> 
{{% /notice %}}

### Step by Step

#### Select the parent folder

Make sure the folder you select contains all the data folders. Any other folder selected (higher or lower in the 
hierarchy will crash the application)!

#### Select the data folder to correct

In the table, simply select all the data folder you want to correct. If a row is highlighted, this folder will
be corrected

#### Select the output folder

The data corrected will be moved into this folder

**Naming convention**

Each data set corrected will be copied inside a folder based on the name of all the images and inside a folder
of the data folder + "_corrected". 

<img src='/tutorial/how_to_run_mcp_detector_correction/images/naming_convention.png' />

### Full correction animation

<img src='/tutorial/how_to_run_mcp_detector_correction/images/mcp_tutorial.gif' />

### Configuration

<img src='/tutorial/how_to_run_mcp_detector_correction/images/configurations_window.png' />

This is where you can define the starting default folder, default output folder and also the **run correction time out**.
The script run in the back requires user input to finish it, because we wanted to allow you to run several job one
after the other without your input, we, using the **time out** value, stop the process manually. During testing, we
found that 35s is long enough to allow all the files to be translater. In case you find that the time out shows up too
early, you may need to increase the time here. 











