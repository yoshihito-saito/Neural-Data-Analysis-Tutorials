# Neural-Data-Analysis-Tutorials
Here is a repository for Neural Data Analysis Tutorials with Allen Brain Observatory.

0. Python basic skills.
1. Explore an Allen dataset.
2. Analyse single neuron metrics.
3. Analyse pairwise metrics.
4. Analyse population metrics.

## Create enviroment 
If you do not have a Python environment, we recommend that you install anaconda or miniconda.

You can install form following. No need to install both. 

For Anaconda: https://www.anaconda.com/download

For miniconda: https://docs.conda.io/en/latest/miniconda.html



## What is a virtual environment? Why do you need to create it?

Each Python library requires a specific version of the other library.

However, sometimes library versions conflict (e.g. library "A" works with library "B ver1.0", but library "C" requires library "B ver2.0". 

In this case, different versions of library 'B' cannot coexist.

So you have to create different environments for libraries 'A' and 'C').

To avoid library contamination, you can use a virtual environment.

Virtual environment allows you to create an isolated environment where you can install specific versions of libraries without
affecting the global Python installation or other environments. 

Here we use conda to create a virtual enviroment.

    Open terminal or anaconda prompt
    
Then type the following to create conda enviroment.

    conda create -n allen python=3.9
    conda activate allen
    pip install allensdk
    pip install ipykernel
    conda install jupyter
    
## Note on Conda Channel Configuration

To ensure compliance with license agreements, the default Conda channels will not be used. Instead, packages will be installed exclusively from the Conda-Forge channel. This configuration minimizes the risk of potential licensing violations and ensures the availability of openly licensed packages.

For details: https://dev.to/kaamisan/using-miniconda-with-conda-forge-to-avoid-anaconda-licensing-issues-5hkj

Make sure to set your Conda environment before making enviroments as follows:

    conda config --show channels
    conda config --add channels conda-forge
    conda config --remove channels defaults
    conda config --set channel_priority strict
    conda config --show channels

