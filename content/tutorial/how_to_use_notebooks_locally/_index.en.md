---
title: How to use the notebooks locally on your computer
weight: 950
pre: "<b>5.10 </b>"

---

<h1 id='top'></a></h1>
When working with your data files we recommend  
[using the notebooks from the analysis machine]({{%relref "/tutorial/how_to_start_notebooks/_index.md#activate-search" %}})
but we also want to provide the flexibility of using the notebooks from your own computer, especially if you want
to modify or implement new notebooks.

We describe here the procedure to follow to bring those notebooks from our repository to your computer and how to
set up your python environment to get all the right libraries. 

## Instructions

We provide here **two** ways to install the notebooks on your computer. The **easy way** using Anaconda Navigator, 
and the **hard way** using command line and terminal, in case you don't want to use anaconda.

* <a href='#easy_way'>Easy way - Anaconda Navigator</a>
* <a href='#geeky_way'>Geeky/hard/fancy way - Command line</a>

<h1 id='easy_way'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> Easy way - Anaconda 

#### Step 1 - Download and install Anaconda Navigator

Download and install the [Anaconda Navigator](https://docs.anaconda.com/anaconda/install/) by selecting the right 
version according to your operating system (OS) and following the instructions found in their web page.

#### Step2 - Download the notebooks

Go to the GitHub page ([https://github.com/neutronimaging/python_notebooks](https://github.com/neutronimaging/python_notebooks)) 
and click the green switch called **Code** and select **Download ZIP**

<img src='/tutorial/how_to_use_notebooks_locally/images/download_repo.png' />

Once the download is done, navigate to the folder where the zip file has been created and simply double click to 
unzip the file. From there feel free to move that folder to its final location on your hard drive. For example,
in my case, I moved it to **/Users/j35/git/**.

#### Step 3 - Create conda environment

 * Start the **Anaconda Navigator** application.
   
<img src='/tutorial/how_to_use_notebooks_locally/images/anaconda_navigator.png' />

 * From there, navigate to **Environments**

<img src='/tutorial/how_to_use_notebooks_locally/images/environments.png' />

 This is where you will import the *environment.yml* file from the **python notebook** folder you just downloaded and
 unzipped. 

 * Click **Import**
 * No need to enter any text in the **name** field. This field will be populated automatically once you have selected the file (see next line).
 * Click the **folder icon** and navigate to the **python notebooks** folder and select the file **environment.yml**.  
 
<img src='/tutorial/how_to_use_notebooks_locally/images/import_new_environment.png' />

The following animation shows you those steps

<img src='/tutorial/how_to_use_notebooks_locally/images/importing_environment.gif' />

#### Step 4 - Select the environment

The new environment created, named **neutron-imaging**, should be selected by default. If not, activate it by clicking
it.

<img src='/tutorial/how_to_use_notebooks_locally/images/check_environment_selected.png' />

#### Step5 - Run the notebooks

All you have to do then is launch the **jupyter notebook engine**. Go to the **Home** page and click the 
LAUNCH button in the **jupyter notebook** box. 

<img src='/tutorial/how_to_use_notebooks_locally/images/launching_jupyter.png' />

A browser window will show up with a list of all your files and folders. Navigate to the jupyter notebook folder
you downloaded and unzip from github and go in the **notebooks** folder. From there, feel free to start any of the
 notebook!
 
<img src='/tutorial/how_to_use_notebooks_locally/images/running_notebooks.gif' />

<h1 id='geeky_way'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> Geeky/hard/fancy way - Command line

* <a href='#for_mac'>for Mac/Linux</a>
* <a href='#for_windows'>for Windows</a>

<h1 id='for_mac'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> for Mac

#### Step 1 - Download or clone the notebooks

Select either one of the two ways to bring the notebooks to your computer

**Download** 

We recommend using the [latest tag (stable)](https://github.com/neutronimaging/python_notebooks/releases/tag/0.1.0) 
version of the notebooks. Click either the **zip** or the **tar.gz** link. 

<img src='/tutorial/how_to_use_notebooks_locally/images/tag.png' />

Go to your download folder and double click the file you just downloaded. Move this folder to your location of choice
on your computer (for example, I used *~/git/* on my computer)

**Clone**

Open a terminal, move to the location where you want to clone (import) the notebooks and then type the clone command
```bash
$ cd ~/git
$ git clone https://github.com/neutronimaging/python_notebooks.git
```

Go to your download folder and double click the file you just downloaded. Move this folder to your location of choice
on your computer (for example, I used *~/git/* on my computer)

#### Step 2 - Install Anaconda on your computer

Anaconda is a free program that will make the installation and management of the python libraries very easy. You can
install either [Anaconda (the full package)](https://www.anaconda.com/products/individual) or just the light version 
called [miniconda3](https://docs.conda.io/en/latest/miniconda.html)

#### Step 3 - Create a virtual python environment

A virtual python environment is like a python version running on your machine but being isolated from the rest of the
system. This way anything you will do in this environment, like installing new libraries, will not affect the rest
of your computer. 

In the following example we chose **neutron_imaging** as the name of our virtual environment. Feel free to replace it 
with whatever name makes more sense to you.

To do so, simply type the following command on your terminal

```
$ conda create -n neutron_imaging python=3
```

Now let's switch to that environment

```
$ conda activate neutron_imaging
```

#### Step 4 - Set up environment

Final step, we need to install all the libraries used by the notebooks. To do so, in your terminal, navigate to 
the notebooks folder your downloaded (tag version)

```
cd ~/git/python_notebooks-0.1.0
```

and execute the installation script **config_conda_env.sh**

```
$ bash config_conda_env.sh
```

This will take a while!

#### Step 5 - launch the notebooks

Last step, start the notebooks

```
$ jupyter notebook
```

Your favorite browser will show up with the notebooks. Enjoy!

<h1 id='for_windows'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> for Windows

#### Step 1 - Install Anaconda

First thing to do will be do download and install anaconda. To do so, go to the 
[anaconda download page](https://www.anaconda.com/products/individual). 

**Click** the **Download** button.
 
<img src='/tutorial/how_to_use_notebooks_locally/images/anaconda_windows_download.png' />

**Click** the **64-Bit or 32-Bit version** according to your machine.

<img src='/tutorial/how_to_use_notebooks_locally/images/anaconda_windows_version.png' />

{{% notice info %}}
If you don't know, there is a higher chance that you are on a 64-Bit machine so give it a try. If you did not use
wisely, the installation will fail and you will need to try the other version.
{{% /notice %}}

Once the download of the program finished, go to your **download** folder and run the installer by **double clicking it**.

<img src='/tutorial/how_to_use_notebooks_locally/images/location_of_anaconda_installer.png' />
<img src='/tutorial/how_to_use_notebooks_locally/images/anaconda_installer.png' />

**Keep the default settings** all the way by clicking **next**.

#### Step 1 - Create conda environment

Once the installation is done you will have a set of new tools in the **Anaconda** menu. Launch the tool called
**Anaconda Powershell Prompt**

<img src='/tutorial/how_to_use_notebooks_locally/images/anaconda_menu.png' />

This is where we are going to import the **imaging notebooks** and installed the **python libraries** you will need
to run the notebooks.

Once the **terminal** comes to life, we are going to create a folder that will contain the code to import. Let's say
we will call it **git** in your home folder

```bash
$ cd ~/
$ mkdir ~/git
$ cd git
```

Now we are going to create a **special python environment** that will allow us to stay away from the native python
of the system, this is a recommended way to work with python packages.

```bash
$ conda create -y -n neutron_imaging python=3.7
```

The name of our environment is called **neutron_imaging** and we are telling the system to install python version 3.7

Just let the terminal install the libraries.

<img src='/tutorial/how_to_use_notebooks_locally/images/conda_shell.png' />

<img src='/tutorial/how_to_use_notebooks_locally/images/conda_activate.png' />

Once the installation is done, we need to activate that environment.

```bash
$ conda activate neutron_imaging
```

#### Step 3 - Import or Clone Notebooks

Select either one of the two ways to bring the notebooks to your computer

**Download** 

We recommend using the [latest tag (stable)](https://github.com/neutronimaging/python_notebooks/releases/tag/0.1.0) 
version of the notebooks. Click either the **zip** or the **tar.gz** link. 

<img src='/tutorial/how_to_use_notebooks_locally/images/tag.png' />

Go to your download folder and double click the file you just downloaded. Move this folder to your location of choice
on your computer (for example, I used *~/git/* on my computer)

**Clone**

Open a terminal, move to the location where you want to clone (import) the notebooks and then type the clone command
```bash
$ cd ~/git
$ git clone https://github.com/neutronimaging/python_notebooks.git
```

Go to your download folder and double click the file you just downloaded. Move this folder to your location of choice
on your computer (for example, I used *~/git/* on my computer)

#### Step 4 - Import all libraries

Now in the anaconda power shell terminal, import all the librairies by typing

```bash
$ conda update -y -n base -c defaults conda
$ conda install -y requests requests-oauthlib numpy scipy pandas scikit-image matplotlib plotly
$ conda install -y nodejs qtpy pyqtgraph astropy
$ conda install -y -c conda-forge ipywe lmfit
$ pip install neutronbraggedge NeuNorm sectorizedradialprofile inflect ImagingReso ipywidgets
$ pip install https://oncat.ornl.gov/packages/pyoncat-1.4.1-py3-none-any.whl
```

```bash
$ jupyter labextension install @jupyter-widgets/jupyterlab-manager
$ jupyter nbextension enable --py widgetsnbextension
$ jupyter lab build
```

You can now launch the **Anaconda Navigator** and select the environment you created and called **neutron_imaging**.

<img src='/tutorial/how_to_use_notebooks_locally/images/select_right_environment.png' />

Now you can go back to the **HOME** menu within the Anaconda Navigator and launch the **Jupyter notebooks**. 

<img src='/tutorial/how_to_use_notebooks_locally/images/jupyter_notebook.png' />

From there, navigate to the folder **~/git/python_notebooks/notebooks/** to get access to all the notebooks!

<img src='/tutorial/how_to_use_notebooks_locally/images/jupyter_notebook2.png' />
