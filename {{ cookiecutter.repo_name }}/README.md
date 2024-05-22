# {{cookiecutter.project_name}}

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


├── Makefile                     <- Makefile with convenience commands like `make data` or `make train`
├── README.md                    <- The top-level README for developers using this project
├── LICENSE                      <- Open-source license if one is chosen
├── .gitignore                   <- Git ignore file for ignoring unnecessary files in version control
│
├── config                       <- Configuration files for the project
│   ├── development.env          <- Environment file for setting environment variables
│   └── logging.conf             <- Logging configuration
│
├── inputs                       <- Folder for storing input files
│
├── docs                         <- Documentation folder
│   ├── index.md                 <- Homepage for your documentation
│   ├── mkdocs.yml               <- Configuration file for mkdocs
│   └── source/                  <- Source directory for documentation files
│
├── models                       <- Folder for storing trained models (if any)
│
├── notebooks                    <- Jupyter notebooks
│
├── pyproject.toml               <- Project configuration file
│
├── requirements.txt             <- The requirements file for reproducing the analysis environment
├── requirements_dev.txt         <- The requirements file for setting up the development environment
│
├── reports                      <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures                  <- Generated graphics and figures to be used in reporting
│
│
├── src                          <- Source code for use in this project
│   ├── __init__.py              <- Makes folder a Python module
│   │
│   ├── agents                   <- Directory for different agents
│   │   ├── __init__.py
│   │   ├── agent_1.py           <- Agent 1  implementation
│   │   ├── agent_2.py           <- Agent 2  implementation
│   │   ├── agent_3.py           <- Agent 3  implementation
│   │  
│   │
│   ├── prompts                  <- Directory for prompt scripts
│   │   ├── __init__.py
│   │   └── prompt_template.py   <- Example prompt script
│   │
│   ├── app                      <- Application directory
│   │   ├── streamlit_app        <- Streamlit application scripts
│   │   │   ├── __init__.py
│   │   │   ├── home.py          <- Homepage for Streamlit app
│   │   │   └── task_specific.py <- Task-specific Streamlit page
│   │   └── telegram_bot         <- Telegram bot scripts
│   │       ├── __init__.py
│   │       ├── bot_main.py      <- Main script for Telegram bot
│   │       └── menu_handler.py  <- Script for handling bot menus
│   │
│   │
│   └── visualisation            <- Scripts to create exploratory and results oriented visualisations
│       ├── __init__.py
│       └── visualise.py


```
