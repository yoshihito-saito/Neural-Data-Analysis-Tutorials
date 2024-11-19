# Neural-Data-Analysis-Tutorials
Here is a repository for Neural Data Analysis Tutorials with Allen Brain Observatory.

0. Python basic skills.
1. Explore an Allen dataset.
2. Analyse single neuron metrics.
3. Analyse pairwise metrics.
4. Analyse population metrics.

## Create enviroment 
If you do not have a Python environment, we recommend that you install miniconda.

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

## Using github for code management

### install packages:
    conda install -c conda-forge nodejs
    pip install jupyterlab-git

### Copying and Editing Another Person's Repository

If you want to copy someone else's GitHub repository into your own account (your "global repository") and edit it, you can use GitHub's **Fork** feature. Here's how to do it specifically using Jupyter Lab.


### 1. Fork the Repository on GitHub
1. **Fork the repository**:
   - Navigate to the repository you want to copy on GitHub.
   - Click the **Fork** button to create a copy of the repository under your own GitHub account.

2. **Copy the forked repository's URL**:
   - After the fork is complete, go to your forked repository in your GitHub account.
   - Click the green **Code** button and copy the repository URL (either HTTPS or SSH).


### 2. Clone the Forked Repository in Jupyter Lab

#### Open a terminal in Jupyter Lab
- In Jupyter Lab, go to **File > New > Terminal**.

#### Clone the repository
- Navigate to the directory where you want to store the repository and run:
  ```bash
  git clone URL for folked-repository
  cd forked-repository


### 3. Edit and Commit Changes

After cloning the repository, you can start editing and managing your changes using Git. Below is a step-by-step guide for editing and committing changes.


#### 1. Editing Files
1. Select the file you want to edit from Jupyter Lab’s file browser, then open it in a notebook or text editor.
2. Save the file after making changes (Ctrl+S).

#### 2. Checking for Changes
1. Click on the **Git icon** in the left sidebar of Jupyter Lab.
2. Files that have been modified or newly created will appear in the **Changed** section.

#### 3. Staging
1. Select the file(s) you want to stage by clicking on them in the Git sidebar.
2. Click the **+ button** to stage the selected changes.
   - Staged files will move to the **Staged** section.

#### 4. Committing Changes
1. **Enter a commit message**:
   - Write a brief description of the changes in the message input field in the Git sidebar.
2. **Execute the commit**:
   - Click the **Commit button** to save the staged changes to the local repository.

#### 5. Pushing Changes
1. Once the commit is complete, the **Push button** will appear in the Git sidebar.
2. Click the **Push button** to send the changes to the remote repository (e.g., GitHub).

