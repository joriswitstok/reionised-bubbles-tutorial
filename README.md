# Reionised bubbles around primordial galaxies

## Introduction

This repository contains all course material, including three ipython notebooks to be followed alongside the exercise sheet. The pre-existing code only serves as a starting point, feel free to adjust it as you see fit.

Working on GitHub, you can fork this repository and create a [codespace](https://github.com/features/codespaces). Alternatively, having navigated to a suitable directory on your local machine, you can obtain all material in this repository directly with `git` on the command line:
```
git clone https://github.com/joriswitstok/reionised-bubbles-tutorial.git
```

## Software requirements

### Option A: Setting up your own python environment

I highly recommend using an [Anaconda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) to manage your python installation. Having installed [Anaconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html#), you can create a new environment from the command line by going into this repository's `auxiliary` directory and using the `bubble3.yml` file listing the necessary modules:
```
cd reionised-bubbles-tutorial/auxiliary
conda env create -f bubble3.yml
conda activate bubble3
```
Then, the following commands first confirm which `pip` installation manager is active, among which should be the one from your new Anaconda environment if it has been properly activated, and install the standalone `spectres` module (NB: you may have to change the directory depending on where `anaconda` is installed):
```
which pip3 # check which pip installation manager is active
~/anaconda3/envs/bubble3/bin/pip3 install spectres # you may have to change the conda installation directory
```
Then, you can start up a Jupyter notebook instance with (again checking if it correctly uses your conda environment):
```
which jupyter
jupyter notebook
```

### Option B: Installing requirements in a pre-existing python environment

If you have an existing python environment you would like to use for running the Jupyter notebooks, you can install the necessary dependencies with the `pip` installation manager by going into this repository's `auxiliary` directory and using the `requirements.txt` file listing the required modules (including the standalone `spectres` module):
```
cd reionised-bubbles-tutorial/auxiliary
which pip3 # check which pip installation manager is active
pip3 install -r requirements.txt
```

## Using custom code modelling the IGM absorption of Lyα

In addition to these required 'standard' packages, we will use some custom, pre-written code from a module called [`lymana_absorption`](https://github.com/joriswitstok/lymana_absorption). First, you'll need to obtain the source code with `git` in an installation directory of choice:
```
git clone https://github.com/joriswitstok/lymana_absorption.git
```
Then, you can follow the repository's instructions to install the code into your Anaconda environment (double checking if it is still activated):
```
cd lymana_absorption
which pip3
~/anaconda3/envs/bubble3/bin/pip3 install .
```