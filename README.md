# MacleodPhaseTwo

This repo is to house the spyder plugin for the Macleod project that can be found here: https://github.com/Reading-Club-Development/macleod

## **Installation**
### To install Spyder:
The easiest way to install Spyder is with the Anaconda Python distribution, which comes with everything you need to get started in an all-in-one package. Download it from its [webpage](https://www.anaconda.com/products/distribution).
For more information, visit its [Installation Guide](https://docs.spyder-ide.org/current/installation.html).


### **Update Spyder using conda:**
From the command line (or Anaconda prompt on Windows), run:
```
conda update anaconda
conda update spyder
```


If this results in an error or does not update Spyder to the latest version, try:
`conda install spyder=5`

### **Install the plugin using pip:**
The macleod_ide plugin is available via test.pypi.org

The plugin can be installed using pip as follows:
`pip install -i https://test.pypi.org/simple/ macleod-ide`

### **Set up a development environment:**
In principle, we could use any Spyder installed within a [conda environment](https://conda.io/projects/conda/en/latest/user-guide/concepts/environments.html#virtual-environments) according to the instructions given in the [installation guide](https://docs.spyder-ide.org/5/installation.html).
However, it is recommended to create a new environment which only has Spyder with the minimum dependencies needed for your plugin.

It can be installed in the following way:
```
$ conda activate base
$ conda install -c conda-forge mamba # Recommended by spyder-ide.org
$ mamba create -n spyder-dev -c conda-forge python=3
$ mamba activate spyder-dev
$ mamba install spyder
```
