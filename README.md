# Visual retrieval for CORD-19

This repository provides instructions on how to run the interactive 3D visualizer to explore articles in the [Cord19 Dataset](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge).

## Instuctions for running the jupyter notebook locally

### Cloning the repository and installing the dependencies

- Clone the repository: `git clone https://github.com/dusangrujicic/cord19-visualizer.git`
- If you use [Poetry](https://python-poetry.org/), navigate to the project directory and run `poetry install`. This will install all the required packages. Otherwise, make sure to install all dependencies specified in the `requirements.txt` file. By running `pip install -r requirements.txt` all dependencies will be installed.

### Downloading the human atlas

Instructions for obtaining the human atlas can be found on the [Voxel-Man website](https://www.voxel-man.com/segmented-inner-organs-of-the-visible-human/).

The obtained model contains images of the male head `head.zip` and torso `innerorgans.zip`. The unzipped directory `innerograns/`, contains the list of objects (organs), and three directories, `CT/`, `labels/`, `rgb/`.

The `innerorgans/rgb/` directory, which constains slices of the human atlas in the form of `.tiff` images, is used in the visualization notebook. It should be moved to the `data/` directory of the project prior to running the notebook.

In case the atlas is not provided in the form of a `data/rgb/` directory with .tif images, running the the notebook will require a mock file of the body volume, which can be obtrained by running:
```shell
gdown https://drive.google.com/uc?id=1IoR6NNQQuyax_VsX_ZCFll4rsSHR0snz -O data/body_volume_mock.npy
```
This mock file contains the rudimentary outline of a human body and can be used to illustrate the concept. In order to visualize the actual organs and tissues as per the 3D human atlas, the Voxel-Man model would need to be obtrained. 

### Fetching the additional data

Once all dependencies are installed, from the main project directory run:

```shell
gdown https://drive.google.com/uc?id=1IoR6NNQQuyax_VsX_ZCFll4rsSHR0snz -O data/hull_faces.npy
gdown https://drive.google.com/uc?id=1wIssW2jLTcdl9-S3zOeMpso5lV5ogDmc -O data/mapped_articles.json
```

### Running the notebook

- If you use [Poetry](https://python-poetry.org/), run `poetry run jupyter notebook` and follow the instructions in the notebook.

- Otherwise, run `jupyter notebook`.
