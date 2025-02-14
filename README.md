[![Version](https://img.shields.io/pypi/v/genepattern-notebook.svg)](https://pypi.python.org/pypi/genepattern-notebook)
[![Documentation Status](https://img.shields.io/badge/docs-latest-brightgreen.svg?style=flat)](https://www.g2nb.org/basic-features/)
[![Docker Pulls](https://img.shields.io/docker/pulls/genepattern/genepattern-notebook.svg)](https://hub.docker.com/r/genepattern/genepattern-notebook/)
[![Join the chat at https://gitter.im/genepattern](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/genepattern/genepattern-notebook?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

GenePattern Notebook for JupyterLab
====================

The [GenePattern Notebook](https://www.g2nb.org/) 
environment gives GenePattern users the ability to interleave text, graphics, and code with 
their GenePattern analyses to create "notebooks" that can be edited, shared, and published. 

GenePattern Notebooks are built on the [Jupyter](https://jupyter.org/) environment 
and extend it so that users can take advantage of its ease of use and ability to encapsulate 
an entire scientific research narrative, without the need to write code. They are a core 
component of the [g2nb](https://www.g2nb.org/) project.

> ### **Looking for classic Jupyter Notebook support?**
> **Jupyter Notebook support in is available, albeit no longer in active development. You can 
> find it in its own branch. [Just click here!](https://github.com/genepattern/genepattern-notebook/tree/notebook)**


### **Prerequisites**

* JupyterLab >= 3.6.0
* ipywidgets >= 8.0.0

# Docker

A Docker image with nbtools and the full JupyterLab stack is available through DockerHub.

```bash
docker pull g2nb/lab
docker run --rm -p 8888:8888 g2nb/lab
```

# Installation

Full installation instructions for casual use are detailed on the 
[GenePattern Notebook website](https://docs.g2nb.org/en/latest/local-installation/). Users should 
also consider the [g2nb Workspace](https://workspace.g2nb.org), which 
provides an install-free cloud deployment of the full suite of g2nb tools, including GenePattern Notebook.

## Development Install

The installation instructions below are intended for developers who want to install the 
project from PIP or GitHub for the purposes of software development.

### Install Python

In order to get the GenePattern Notebook working you will first need to install a compatible 
version of Python. This means you will need Python 3.6+. We recommend using the 
[Anaconda](https://www.anaconda.com/download/#macos) Python distribution. This is 
a scientific version of Python that ships with many of the most popular Python packages for 
science, math and data analysis (ex: NumPy, SciPy, Pandas, Matplotlib, IPython, etc.).

### Install GenePattern Notebook from GitHub

Copy the contents of genepattern-notebook/extension to your development computer and ensure 
that the resulting directory if on your Python path. To test this, open Python and try to 
*import genepattern*. If this is successful, you have a copy of the extension available.

If you don't already have Jupyter installed, you can install it from PIP by running:

> pip install jupyter

From here go to the "Load the GenePattern extension" step below.

### Install GenePattern Notebook from PIP or Conda

The easiest way to install GenePattern Notebook is through either PIP or conda. It can be installed by 
executing one of the following commands:

```bash
pip install genepattern-notebook
```

*or*

```bash
conda install -c genepattern genepattern-notebook
```

### Load the nbtools extension

```bash
# Clone the nbtools repository
git clone https://github.com/g2nb/nbtools.git
cd nbtools

# Install the nbtools JupyterLab prototype
pip install .
jupyter labextension install .
```

### Launch Jupyter

Finally, you may launch JupyterLab by issuing the following command at the terminal:

> jupyter lab

This will start up the notebook kernel and launch your web browser pointing to the Notebook.

# Related Repositories

The following GitHub repositories contain code or other data related to the GenePattern 
Notebook environment.

* [g2nb](https://github.com/g2nb/g2nb): A meta-package which installs all of the g2nb tools and extensions.
* [genepattern-python](https://github.com/genepattern/genepattern-python): The GenePattern 
    Library allows for programmatic access to GenePattern from Python, and is used by 
    GenePattern Notebook behind the scenes.
* [nbtools](https://github.com/g2nb/nbtools): The Notebook Tool Manager 
    is a tool-agnostic interface and registry for searching, browsing and launching available 
    notebook tools in a Jupyter environment.
* [jupyter-wysiwyg](https://github.com/g2nb/jupyter-wysiwyg): A WYSIWYG editor for 
    markdown cells.
* [example-notebooks](https://github.com/g2nb/example-notebooks): A repository of example notebooks that 
    demonstrate functionality or analysis techniques in the GenePattern Notebook environment.
* [workspace](https://github.com/g2nb/workspace): Scripts, services 
    and other infrastructure used in the operation of the GenePattern Notebook Repository.

# Code of Conduct

We are dedicated to providing a harassment-free experience for all members of the GenePattern community, regardless of gender, gender identity and expression, sexual orientation, disability, physical appearance, body size, age, race, or religion. We do not tolerate harassment of participants in any form. This code of conduct applies to all GenePattern spaces, including the Google Group, our Git repositories, and our social media accounts, both online and off. Anyone who violates this code of conduct may be sanctioned or expelled from these spaces at the discretion of the GenePattern team.

For more details, see our [Code of Conduct](https://github.com/genepattern/genepattern-notebook/blob/master/Code_of_Conduct.md).
