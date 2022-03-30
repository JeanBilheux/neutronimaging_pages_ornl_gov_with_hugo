---
title: Bragg Edge Strain Mapping
weight: 650
pre: "<b>5.6.2 </b>"
---

The following tutorial will guide, step by step, in a full Bragg Edge Strain Mapping using the in-house program
called **iBeatles** (Imaging Bragg Edge Analysis Tools for Engineering Structure).

<img src='/tutorial/how_to_do_bragg_edge_strain_mapping/images/a_ibeatles.png' />

{{% notice warning %}}
## for the beta tester

If you found any issue or would like to request a new feature, please edit the following [ticket #108](https://github.com/ornlneutronimaging/iBeatles/issues/108) in the iBeatles
repository
<img src='/tutorial/how_to_do_bragg_edge_strain_mapping/images/ticket_108.png' />

{{% /notice %}}

## How to Install iBeatles

{{% notice info %}}
iBeatles has been developed on a Mac and is then, for now, optimized for Mac OS, but should also work on Linux and 
Windows OS. The easy-installation process is right now only working on Mac. Linux and Windows users will require
to install the library iBeatles from source (repository) and installed the various dependencies libraries themselves. 
Please contact <a href="/credits#jean_bilheux">Jean Bilheux</a> if you need help. 
{{% /notice %}}

#### Install Conda

iBeatles is available as conda package for Mac only right now (testing phase). In order to install iBeatles, you 
need to have [**conda**](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html) 
installed on your mac. You can either download and installed the full version, Anaconda, or
the light version, miniconda. 

#### Create and Activate Conda environment

We need to create a conda environment in order to not interfere with any python version you have running on your machine.
Open a **terminal** and type the command

```linux
conda create -n testing_ibeatles_38 python=3.8
``` 

We now need to activate this environment

```linux
conda activate testing_ibeatles_38
```

#### Installation of iBeatles via conda

Because [iBeatles is available as conda package](https://anaconda.org/neutronimaging/ibeatles), its installation is 
very easy, just type

```commandline
conda install -c neutronimaging ibeatles
```

#### Installation of dependencies

iBeatles uses the following packages currently not available as conda packages, so you need to install them manually
via pip

```commandline
pip install neutronbraggedge changepy NeuNorm
```

## How to Launch iBeatles

```commandline
python -m ibeatles
```

<hr>

## Input Requirements

### Files

The current version of the application will required the following input files to work

 * set of images (tiff or fits). If not already normalized, you will need to provide the **open beam (OB)** files as
 well.
 * a 2 columns **time spectra** ascii file. First column being the time offset of the corresponding image index. The
 second column is ignored. 

 ### Settings

 * detector offset
 * distance sample to source
 
Those will be used to convert the time offset into lambda.

<hr>

## Overview of the Application

### Steps

### Working with Sessions

### Log Book

<hr>

## Step by Step Tutorial

This tutorial is going to take you the various steps required to perform a full strain mapping analysis. 

 * working with raw data
 * working with normalized data

### Load the Data

### Normalized the Data

### Load Normalized Data

### Rotate

### Select Bins

### Bragg Edge Fitting

#### March-Dollase Algorithm
 
#### Kropff Algorithm

### Strain Mapping


