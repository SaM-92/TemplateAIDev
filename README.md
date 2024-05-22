# An up-to-date Cookiecutter template for PI Team

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._

#### Requirements to use the cookiecutter template:


```bash
$ pip install cookiecutter
```

or

```bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```

### To start a new project, run:

---

 `` cookiecutter  https://azdev.iesve.com/Integrated%20Environmental%20Solutions/PIT/_git/code_template_for_pi``

Then specify the required names. 

Then go to that file directory the do the below:

You need to create a conda environment

`` conda create -n your_env_name python=x.x``

Then activate it:

``conda activate your_env_name``

Then you need to intall requirements:

``pip install -r requirements_dev.txt``

In your terminal do this as well so Python can understand the packages: 

``$Env:PYTHONPATH += ";C:\path\to\{{ cookiecutter.repo_name }}\src"``


## Making Documentation

There is a markdonw file in ``docs/source`` which is called ``model_documentation.md``, in that file you need to specify addresses of your functions to it, so the relevant files can be cerated. 

Then run this code in the terminal from the main directory: 

``mkdocs build --config-file docs/mkdocs.yml``

then go into ``docs`` folder via doing ``cd  .\docs\`` then do this: 

``mkdocs serve``


### The resulting directory structure

---

The directory structure of your new project looks like this:

```
├── LICENSE
├── Makefile           <- Makefile with commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default Sphinx project; see sphinx-doc.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
├── src                <- Source code for use in this project.
│   ├── __init__.py    <- Makes src a Python module
│   │
│   ├── data           <- Scripts to download or generate data
│   │   └── make_dataset.py
│   │
│   ├── features       <- Scripts to turn raw data into features for modeling
│   │   └── build_features.py
│   │
│   ├── models         <- Scripts to train models and then use trained models to make
│   │   │                 predictions
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   └── visualization  <- Scripts to create exploratory and results oriented visualizations
│       └── visualize.py
│
└── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io
```

### Installing development requirements

---

    pip install -r requirements.txt
