---
title: List Bragg Edges of an Element
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: list_element_bragg_edges.ipynb

## Description

This notebook lists the given number of hkl, d-spacing and Bragg Edges values for one of the listed element.

<img src='/tutorial/notebooks/list_element_bragg_edges/images/list_bragg_edges_result.png' />

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

## How to Use It?

### Select the entries

Select the **element** and the **number of data** you want to see.

<img src='/tutorial/notebooks/list_element_bragg_edges/images/select.png' />

### Table Result

The next cell will display the following information

 - name of the material you selected
 - lattice value
 - crystal structure
 - if the program used the local metadata table or retrieved the information from the NIST web site directly
 - d-spacing and Bragg edges values for each hkl
 
 <img src='/tutorial/notebooks/list_element_bragg_edges/images/table.png' />

### Export table

You have the option to export the table information as a CSV (comma separated file format). 

Select the **output folder** where the file will be created. The file will then be created automatically 
using the following file name convention

**bragg_edges_of\_\<name_of_element\>.txt**

<img src='/tutorial/notebooks/list_element_bragg_edges/images/export_file.png' />
