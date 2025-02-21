# Reionised bubbles around primordial galaxies

## Introduction

This repository contains all course material, including three ipython notebooks to be followed alongside the exercise sheet. The pre-existing code only serves as a starting point, feel free to adjust it as you see fit.

From the command line, you can obtain all material in this repository directly with `git`:
```
git clone git@github.com:joriswitstok/reionised-bubbles-tutorial.git
```

## Software requirements

I highly recommend using an Anaconda environment to manage your python installation. Using the command line (you may have to change the directory where anaconda is installed), you can create a new environment from the command line with
```
cd auxiliary
conda env create -f bubble3.yml
conda activate bubble3
```
Then, the following commands first tell you which `pip` installation manager is active and install the standalone `spectres` module:
```
which pip3
~/anaconda3/envs/bubble3/bin/pip3 install spectres
```
Then, you can start up a Jupyter notebook instance with (again checking if it correctly uses your conda environment):
```
which jupyter
jupyter notebook
```

## Using custom code modelling the IGM absorption of Lyα

We will use pre-written code from a module called [`lymana_absorption`](https://github.com/joriswitstok/lymana_absorption). First, you can obtain the source code with `git`:
```
git clone https://github.com/joriswitstok/lymana_absorption.git
```
Then, you can follow the repository's instructions to install the code into your anaconda environment (double checking if it is still activated):
```
cd lymana_absorption
which pip3
~/anaconda3/envs/bubble3/bin/pip3 install .
```