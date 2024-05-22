# }

{{cookiecutter.description}}


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

## Project structure
```
The directory structure of the project looks like this:

├── Makefile             <- Makefile with convenience commands like `make data` or `make train`
├── README.md            <- The top-level README for developers using this project.
├── docs                 <- Documentation folder
│   │
│   ├── index.md         <- Homepage for your documentation
│   │
│   ├── mkdocs.yml       <- Configuration file for mkdocs
│   │
│   └── source/          <- Source directory for documentation files
│
├── models               <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks            <- Jupyter notebooks.
│
├── pyproject.toml       <- Project configuration file
│
├── reports              <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures          <- Generated graphics and figures to be used in reporting
│
├── requirements.txt     <- The requirements file for reproducing the analysis environment
 ├── requirements_dev.txt <- The requirements file for reproducing the analysis environment
│
├── src  <- Source code for use in this project.
│   │
│   ├── __init__.py      <- Makes folder a Python module
│   │
│   ├── data             <- Scripts to download or generate data
│   │   ├── __init__.py
│   │   └── make_dataset.py
│   │
│   ├── models           <- model implementations, training script and prediction script
│   │   ├── __init__.py
│   │   ├── predict_model.py
│   │   ├── forecast_model.py
│   ├── visualization    <- Scripts to create exploratory and results oriented visualizations
│   │   ├──__init__.py
│   │   └── visualize.py
│
└── LICENSE              <- Open-source license if one is chosen
```
