# Visual retrieval for CORD-19

This repository provides instructions on how to run the interactive 3D visualizer to explore articles in the Cord19 Dataset (https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge).

## Instuctions for running the jupyter notebook locally

### Cloning the repository and installing the dependencies

- Clone the repository: `git clone https://github.com/gorjanradevski/covid19-visualizer.git`
- If you use [Poetry](https://python-poetry.org/), navigate to the project directory and run `poetry install`. This will install all the required packages.

- Otherwise, make sure to install all dependencies specified in the `requirements.txt` file. For example, by running `pip install -r requirements.txt` you will have all required packages locally.

### Fetching the data

- Once all dependencies are installed, from the main project directory run:

```shell
poetry run gdown https://drive.google.com/uc?id=19b_TP8CKkBPoziiO8m5sVsKSTgmAk-kZ -O data/body_volume.npy
poetry run gdown https://drive.google.com/uc?id=1Y4v3vePcH6fqyBpdxWHkE1kFEca4BCmO -O data/hull_faces.npy
poetry run gdown https://drive.google.com/uc?id=1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1 -O data/mapped_articles.json 
```

if you use [Poetry](https://python-poetry.org/), otherwise:

```shell
gdown https://drive.google.com/uc?id=19b_TP8CKkBPoziiO8m5sVsKSTgmAk-kZ -O data/body_volume.npy
gdown https://drive.google.com/uc?id=1Y4v3vePcH6fqyBpdxWHkE1kFEca4BCmO -O data/hull_faces.npy
gdown https://drive.google.com/uc?id=1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1 -O data/mapped_articles.json
```

- Other option is to download the three needed files [body_volume.npy](https://drive.google.com/file/d/1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1/view?usp=sharing), [hull_faces.npy](https://drive.google.com/file/d/1Y4v3vePcH6fqyBpdxWHkE1kFEca4BCmO/view?usp=sharing) and [mapped_articles.json](https://drive.google.com/file/d/1jnWJ4hF0T-aMYXpLuBe6e-QcdvnFEAo1/view?usp=sharing) directly from Google Drive and move them to the `data/` directory.

### Running the notebook

- If you use [Poetry](https://python-poetry.org/), run `poetry run jupyter notebook` and follow the instructions in the notebook.

- Otherwise, run `jupyter notebook`.

## Authors

Dusan Grujicic, [Gorjan Radevski](http://gorjanradevski.github.io/), [Tinne Tuytelaars](https://homes.esat.kuleuven.be/~tuytelaa/), [Matthew Blaschko](https://homes.esat.kuleuven.be/~mblaschk/)
