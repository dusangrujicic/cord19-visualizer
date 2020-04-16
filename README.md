# Visual retrieval for CORD-19

This repository provides instructions on how to run the interactive 3D visualizer to explore articles in the Cord19 Dataset (https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge).

## Instuctions for running the jupyter notebook locally

### Cloning the repository and installing the dependencies

- Clone the repository: `git clone https://github.com/dusangrujicic/cord19-visualizer.git`
- If you use [Poetry](https://python-poetry.org/), navigate to the project directory and run `poetry install`. This will install all the required packages. Otherwise, make sure to install all dependencies specified in the `requirements.txt` file. By running `pip install -r requirements.txt` all dependencies will be installed.

### Downloading the human atlas

Instructions for obtaining the human atlas can be found on the [Voxel-Man website] (https://www.voxel-man.com/segmented-inner-organs-of-the-visible-human/)

The obtained model contains images of the male head (head.zip) and torso (innerorgans.zip). The unzipped directory innerograns/, contains the list of objects (organs), and three directories, CT/, labels/, rgb/.

The innerorgans/rgb/ directory, which constains slices of the human atlas in the form of .tif images, is used in the visualization notebook. It should be moved to the data/ directory of the project prior to running the notebook.


### Fetching the data

- Once all dependencies are installed, from the main project directory run:

```shell
gdown https://drive.google.com/uc?id=1Y4v3vePcH6fqyBpdxWHkE1kFEca4BCmO -O data/hull_faces.npy
gdown https://drive.google.com/uc?id=1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1 -O data/mapped_articles.json 
```

- Another option is to download the three needed files [hull_faces.npy](https://drive.google.com/file/d/1Y4v3vePcH6fqyBpdxWHkE1kFEca4BCmO/view?usp=sharing) and [mapped_articles.json](https://drive.google.com/file/d/1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1/view?usp=sharing) directly from Google Drive and move them to the `data/` directory.

### Running the notebook

- If you use [Poetry](https://python-poetry.org/), run `poetry run jupyter notebook` and follow the instructions in the notebook.

- Otherwise, run `jupyter notebook`.
