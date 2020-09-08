---
title: Extract Metadata from SANS ReductionLog
post: " <i class='fa fa-battery-full'></i>"
pre: "- "

---

**Notebook name**: extract_sans_reductionlog_metadata.ipynb

## Description

This notebook creates an ASCII file of any of the metadata selected in the ReductionLog file.
This file is created at the end of each reduction and contain a lot of information about
the reduction process. Metadata from all ReductionLog files are listed side by side in a comma
separated format as shown here. 

<img src='/tutorial/notebooks/extract_sans_reductionlog_metadata/images/example_of_output.png' />

In this format, all the metadata selected of a given input file are on the same row. You will then have
as many rows as input files selected.

## Step by Step Demo

### Select your instrument

Select your HFIR SANS instrument. This will allow the program to start directly from the instrument
folder. 

<img src='/tutorial/notebooks/extract_sans_reductionlog_metadata/images/select_instrument.png' />

### Select the ReductionLog files

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
all the ReductionLog files (*.hdf) you want to use. 

Once you selected all those files, the notebook will automatically display all the metadata you
can extract. This list of metadata has been provided by the instrument team. This allows to 
only display the metadata of interest and hide most of the one you don't really care.

### Select list of metadata to extract

Use a combination of CLICK, SHIFT + CLICK and CTRL + CLICK to make sure you selected all the metadata.

<img src='/tutorial/notebooks/extract_sans_reductionlog_metadata/images/select_metadata.gif' />

### Select output folder

Using the [folder selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
the folder where you want to create the ascii file. 
