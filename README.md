# Visualizer for the Covid19 dataset

This repository provides instructions how to run the interactive 3D visualizer to explore Covid19 papers.

## Instuctions for running the jupyter notebook locally

### Cloning the repository and installing the dependencies

- Clone the repository: `git clone https://github.com/gorjanradevski/covid19-visualizer.git`
- If you use [Poetry](https://python-poetry.org/), navigate to the project directory and run `poetry install`. This will install all the required packages.

- Otherwise, make sure to install all dependencies specified in the `requirements.txt` file. For example, by running `pip install requirements.txt` you will have all required packages locally.

### Fetching the data

- Once all dependencies are installed, from the main project directory run:

```shell
poetry run gdown https://drive.google.com/uc?id=151jJIOuB_MUiFnJ5VM7Je6IcbFbNH-KL -O data/body_volume_mini.npz
poetry run gdown https://drive.google.com/uc?id=1wANDPte4_OTIAwq4SREknnCIYTpbgYDm -O data/data_frame_small.json
```

if you use [Poetry](https://python-poetry.org/), otherwise:

```shell
gdown https://drive.google.com/uc?id=151jJIOuB_MUiFnJ5VM7Je6IcbFbNH-KL -O data/body_volume_mini.npz
gdown https://drive.google.com/uc?id=1wANDPte4_OTIAwq4SREknnCIYTpbgYDm -O data/data_frame_small.json
```

- Other option is to download the two needed files [body_volume_mini.npz](https://drive.google.com/file/d/151jJIOuB_MUiFnJ5VM7Je6IcbFbNH-KL/view?usp=sharing), and [data_frame_small.json](https://drive.google.com/file/d/1wANDPte4_OTIAwq4SREknnCIYTpbgYDm/view?usp=sharing) directly from Google Drive and move them to the `data/` directory.

### Running the notebook

- If you use [Poetry](https://python-poetry.org/), run `poetry run jupyter notebook` and follow the instructions in the notebook.

- Otherwise, run `jupyter notebook`.

## Instructions for running the notebook on Google Colab

Open the notebook from the link bellow and follow the instructions in the notebook. However, it is possible that Google Colab is not able to run the interactive visualization due to backend issues. If that is the case, you have to follow the instructions for running the notebook locally.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gorjanradevski/covid19-visualizer/blob/master/visualizer-demo.ipynb)

## Authors

Dusan Grujicic, [Gorjan Radevski](http://gorjanradevski.github.io/), [Tinne Tuytelaars](https://homes.esat.kuleuven.be/~tuytelaa/), [Matthew Blaschko](https://homes.esat.kuleuven.be/~mblaschk/)