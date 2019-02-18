---
title: Metadata Ascii Parser
post: "<i class='fa fa-battery-full'></i> "
pre: "- "

---

**Notebook name**: metadata_ascii_parser.ipynb

## Description

Because of the large variety of sample environment used, we need to face a large variety of metadata files outputs. 
Those metadata files contain the sample environment data, such as **temperature of a furnace**, **pressure of a cell**, 
**voltage of a power supply**, etc. This notebook will allow you to select this metadata and isolate the set of 
information you want to retrieve. A new ascii file will then be created in a more common format that other notebooks
will be able to use. 

{{% notice warning %}}
If your metadata file can not be parsed by this program, this means we need to write a new plugin for that particular 
file, please contact <a href="/en/credits#jean_bilheux">Jean Bilheux</a>.
{{% /notice %}}

The metadata file currently supported by this application looks like this: 

<img src='/tutorial/notebooks/metadata_ascii_parser/images/metadata_file_1.png' />

and will create the following type of output file

<img src='/tutorial/notebooks/metadata_ascii_parser/images/output.png' />

## Start the notebook

If you need help accessing this notebook, check the [How To > Start the python
notebooks](/en/tutorial/how_to_start_notebooks) tutorial.

### Select your IPTS

{{% notice info %}}
Need help using the [IPTS selector]({{%relref "/tutorial/notebooks/select_ipts/_index.md#activate-search" %}})?
{{% /notice %}}

### Select the metadata file

Using the [file selection tool]({{%relref "/tutorial/notebooks/file_selector/_index.md#activate-search" %}}), select 
your metadata file. 

### Select the infos you want to keep

The program will list the name of each column of metadata, as well as a data/time columns created by the program
 itself. Select the metadata you want to keep (any number of columns is allowed). 
 
<img src='/tutorial/notebooks/metadata_ascii_parser/images/metadata_selection.gif' />
 
Use **SHIFT** or **COMMAND + CLICK** to select more than one metadata. 

### Select output folder and filename
  
It is now time to export the new ascii metadata file. 

Define the output file name. The extension *.txt* will be automatically added if you don't specify it. Then select
the output folder. 

<img src='/tutorial/notebooks/metadata_ascii_parser/images/output_folder_filename.png' />

The new comma separated ascii file will have the following columns

**Index, timestamp (s), metadata you selected ...**

<img src='/tutorial/notebooks/metadata_ascii_parser/images/output_detail.png' />



