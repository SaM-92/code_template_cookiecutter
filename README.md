# AI-Enabled Software Systems Cookiecutter Template

_A logical, standardized, and flexible project structure designed for developing and sharing AI, data science, and LLM (Language Model) projects._

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

 `` cookiecutter  https://github.com/SaM-92/code_template_cookiecutter/``

Then specify the required names. 

Then go to that file directory the do the below:


## Setup Instructions

### 1. Create and Activate Conda Environment

To set up the project environment, follow these steps:

1. **Create Conda Environment**

   Use the `make create_environment` command to create a conda environment:

   ```sh
   make create_environment
   ```

This command will create a new conda environment named after your project with the specified Python version.

2. \*\*\*Activate Conda Environment

Activate the newly created environment:

```sh
   conda activate {{ cookiecutter.project_name }}
```

### 2. Install Dependencies

Once the environment is activated, install the required dependencies:

1. Install Python Dependencies

Use the make requirements command to install the required Python packages:

```sh
make requirements
```

2. Install Developer Dependencies

If you need to install the developer dependencies as well, use the make dev_requirements command:

```sh
make dev_requirements
```

### 3. Set PYTHONPATH

To ensure Python can understand the packages, set the PYTHONPATH environment variable:

For Windows PowerShell:

```sh
$Env:PYTHONPATH += ";C:\path\to\{{ cookiecutter.repo_name }}\src"
```

For Unix-like systems (bash):

```sh
 export PYTHONPATH="$PYTHONPATH:/path/to/{{ cookiecutter.repo_name }}/src"
```

## Makefile Commands

Here are some useful make commands available in this project:

1. Set up python interpreter environment

```sh
make create_environment
```

2. Install Python Dependencies

```sh
make requirements
```

3. Install Developer Python Dependencies

```sh
make dev_requirements
```

4. Delete all compiled Python files

```sh
make clean
```

6. Process raw data into processed data

```sh
 make data
```

8. Build documentation

```sh
make build_documentation
```

7. Serve documentation

```sh
make serve_documentation
```

## Help

For a list of all available make commands, run:

```sh
make help
```






### The resulting directory structure

---

The directory structure of your new project looks like this:

```
├── Makefile                     <- Makefile with convenience commands like `make data` or `make train`
├── README.md                    <- The top-level README for developers using this project
├── LICENSE                      <- Open-source license if one is chosen
├── .gitignore                   <- Git ignore file for ignoring unnecessary files in version control
│
├── config                       <- Configuration files for the project
│   ├── development.env          <- Environment file for setting environment variables
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
│   ├── main.py                  <- Main script for orchestrating
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

