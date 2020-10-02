---
title: How to use the notebooks in your computer
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

* <a href='#for_mac'>for Mac/Linux</a>
* <a href='#for_windows'>for Windows</a>

<h1 id='for_mac'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> for Mac

#### Step1 - Download the notebooks

We recommend using the [latest tag (stable))(https://github.com/neutronimaging/python_notebooks/releases/tag/0.1.0) 
version of the notebooks. Click either the **zip** or the **tar.gz** link. 

<img src='/tutorial/how_to_use_notebooks_locally/images/tag.png' />

#### Step2 - Move folder to new location

Go to your download folder and double click the file you just downloaded. Move this folder to your location of choice
on your computer (for example, I used *~/git/* on my computer)

#### Step3 - Install Anaconda on your computer

Anaconda is a free program that will make the installation and management of the python libraries very easy. You can
install either [Anaconda (the full package)](https://www.anaconda.com/products/individual) or just the light version 
called [miniconda3](https://docs.conda.io/en/latest/miniconda.html)

#### Step4 - Create a virtual python environment

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

#### Step5 - Set up environment

Final step, we need to install all the librairies used by the notebooks. To do so, in your terminal, navigate to 
the notebooks folder your downloaded (tag version)

```
cd ~/git/python_notebooks-0.1.0
```

and execute the installation script **config_conda_env.sh**

```
$ bash config_conda_env.sh
```

This will take a while!

#### Step 6 - launch the notebooks

Last step, start the notebooks

```
$ jupyter notebook
```

Your favorite browser will show up with the notebooks. Enjoy!

<h1 id='for_windows'></h1>
### <a href='#top' class='fa fa-arrow-up'></a> for Windows

Coming soon!