---
title: Run a jupyter notebook
weight: 4
---

<h1 id='top'></a></h1>
Our jupyter python notebooks are very straighforward to use but there are just a few **key points** you need to know.

 * <a href='#notebook_layout'>notebook layout</a>
 * <a href='#run_the_notebook'>run the notebook</a>
 * <a href='#modify_the_notebook'>modify the notebook</a>

<h1 id='notebook_layout'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> Notebook layout

<img src='/tutorial/how_to_run_notebooks/images/notebook_legend.png' />

<h1 id='run_the_notebook'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> Run the notebook

#### Execute cells

The notebooks must be run from **top** to **bottom**. Place the cursor in the first cell and either click the
<li class='fa fa-step-forward'></li> icon, or by using the keyboard shortcut **SHIFT + ENTER**.

This is showing a busy notebook with the background cell green and the full circle at the top right corner of the notebook.

<img src='/tutorial/how_to_run_notebooks/images/busy_notebook.png' />

#### Folder Navigation

At least one time per notebook, you will need to select a folder or one or more files. This widget will look like this
<img src='/tutorial/how_to_run_notebooks/images/file_folder_browser.png' />

The UI is pretty self explanatory but you just need to know that:

 * In the file/folder listing widget

    * *.* means refresh of the current location
    * *..* means moving up one directory, or folder.

 * The file or folder will be really selected only once you have clicked the **Select**
button at the bottom right corner.

 * To select more than one file (when this option is available), **CLICK** first file then **SHIFT + CLICK**
 the last one. Or **ALT + CLICK** to individually select each file.

#### Output and widgets

The cell is then executed and depending on the contain of this one, you may see or not an output to the cell.
The output is always displayed just below the cell ran. In some of our notebooks you will see **widgets** that you will
need to interact with. Here are a few examples of widgets you may encounter in your notebook.

<img src='/tutorial/how_to_run_notebooks/images/widget_1.png' />
<img src='/tutorial/how_to_run_notebooks/images/widget_2.png' />

In some notebooks, the output may even show up in the back of the notebook (the default cell output will give you a
message that let you know where to look). Those outside widgets are more complex user interface such as the one shown
here.

<img src='/tutorial/how_to_run_notebooks/images/widget_3.png' />

<h1 id='modify_the_notebook'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> Modify the notebook
