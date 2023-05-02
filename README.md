# MacleodPhaseTwo

This repo is to house the spyder plugin for the Macleod project that can be found here: https://github.com/Reading-Club-Development/macleod

## **Installation**

### For Linux and macOS 

**Install Spyder:**  
The easiest way to install Spyder is with the Anaconda Python distribution, which comes with everything you need to get started in an all-in-one package. Download it from its [webpage](https://www.anaconda.com/products/distribution). For our purposes, either Anaconda or Miniconda will work.
For more information, visit its [Installation Guide](https://docs.spyder-ide.org/current/installation.html).

**Update Spyder using conda:**
From the command line (or Anaconda prompt on Windows), run:
```
conda update anaconda
conda update spyder
```

If this results in an error or does not update Spyder to the latest version, try:
`conda install spyder=5`

**Set up a development environment:**  
In principle, we could use any Spyder installed within a [conda environment](https://conda.io/projects/conda/en/latest/user-guide/concepts/environments.html#virtual-environments) according to the instructions given in the [installation guide](https://docs.spyder-ide.org/5/installation.html).
However, it is recommended to create a new environment which only has Spyder with the minimum dependencies needed for your plugin.
```
conda activate base
conda create -n spyder-dev -c conda-forge python=3.11
conda activate spyder-dev
```
**Install the plugin using pip:**    
The macleod_ide plugin is available via pypi.org

The plugin can be installed using pip as follows:
`pip install macleod-ide`

**Launch Spyder:**  
To launch Spyder, use the command:
`spyder`

### For Windows:
**Install Spyder:**  
The easiest way to install Spyder is with the Anaconda Python distribution, which comes with everything you need to get started in an all-in-one package. Download it from its [webpage](https://www.anaconda.com/products/distribution). For our purposes, either Anaconda or Miniconda will work.
For more information, visit its [Installation Guide](https://docs.spyder-ide.org/current/installation.html).

From the command line, navigate to the Anaconda folder. By default the location will be:
C:\Users\[user]\anaconda3\Scripts

**Activate a conda shell:**  
Anaconda offers several shells, initialize the shell of your choice with the following command:
`conda init [shell]`  
Example: `conda init cmd.exe`

For more information on conda shells, use:
`conda init --help`

**Update Spyder using conda:**  

From the command line, run:
```
conda update anaconda
conda update spyder
```

If this results in an error or does not update Spyder to the latest version, try:
`conda install spyder=5`

**Set up a development environment:**  
In principle, we could use any Spyder installed within a [conda environment](https://conda.io/projects/conda/en/latest/user-guide/concepts/environments.html#virtual-environments) according to the instructions given in the [installation guide](https://docs.spyder-ide.org/5/installation.html).
However, it is recommended to create a new environment which only has Spyder with the minimum dependencies needed for your plugin.
```
conda activate base
conda create -n spyder-dev -c conda-forge python=3.11
conda activate spyder-dev
```

**Install the plugin using pip:**    
The macleod_ide plugin is available via pypi.org

The plugin can be installed using pip as follows:
`pip install macleod-ide`

**Launch Spyder:**  
To launch Spyder, use the command:
`spyder`

## Troubleshooting
### For Windows
A common error encountered when configuring Anaconda on Windows is the error:  
`pip is configured with locations that require TLS/SSL, however the ssl module in Python is not available`

The easiest way we have found to resolve this issue is to copy four files **from** C:\Users\[user]\Anaconda3\Library\bin **to** C:\Users\MyUser\Miniconda3\DLLs  

The four files to copy are:
* libcrypto-1_1-x64.dll
* libcrypto-1_1-x64.pdb
* libssl-1_1-x64.dll
* libssl-1_1-x64.pdb

