# DSR Teaching: How to SetUp a Data Science Project


![image](./assets/image.jpg)

## Project Description
The purpose of this mini-project is to show how to set up a data science project

It follows these steps: 
1. Create a new repository in GitHub
2. Clone the repository on your computer
3. Set your Readme, .gitignore & requirements file
    ❗️Push your changes❗️
4. Create a Conda Environment
5. Install needed packages
6. Make the environment visible in Jupyter Notebook / Jupyter Lab
7. Start Jupyter Lab / Jupyter Notebook
8. Install a Code Formatter
            
 
### Tech Stack 
* Python
* Jupyter Lab & Jupyter Notebook
* PyCharm
* Github
    * example for file structure - pipeline and project workflow template of  [DSSG](https://github.com/dssg/hitchhikers-guide/tree/master/sources/curriculum/0_before_you_start/pipelines-and-project-workflow). 

## Detailed Instructions 

### 1. Create a Repo in GutHub

* you can create a repo in GutHub by following these [instructions](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/create-a-repo
)
* Initialise the repository with both a readme and a .gitignore file
    * the readme is what you are reading now ;). It contains useful information about the project and how to set it up
    * the .gitignore file contains all files and folders that should NOT be pushed to the repository, i.e. they should remain hidden. Examples are: files containing passwords, folders containing raw data. Select the template for Python.  
![readme_gitignore](./assets/readme_gitignore.png)


### 2. Clone the New Repository
In your terminal:
* go to the folder, in which you keep your repositories. Use `cd <YOUR FOLDER NAME>`
* execute `git clone https://github.com/<YOUR USERNAME>/<YOUR REPO NAME>.git`
* if you need any help, see this [tutorial](https://help.github.com/articles/cloning-a-repository/).


### 3. Set your README, .gitignore & requirements file
* README
    * idea for [structure](https://github.com/Iskriyana/data-science-project-template)
    * help for the [formatting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)
    * PyCharm comes in handy when creating the file
* .gitignore
    * [documentation](https://git-scm.com/docs/gitignore)
    * collection of [.gitignore templates](https://github.com/github/gitignore). Relevant for you is the Python one
* requirements.txt
    * create a simple empty `.txt` file
    * every time you install a new package, add it with its version to this file in the format `package==version
    * there are also automatic ways to create this file. However, they are some times either too detailed or do not include everything
        * create with pip: `pip freeze > requirements.txt`
        * create with [PyCharm](https://www.jetbrains.com/help/pycharm/managing-dependencies.html#configure-requirements)
* after setting the files, push to repository by typing in your terminal
    * `git add .`
    * `git commit -m '210104_repo_setup'`
    * `git push origin main`
    
### 4. Create a Conda Environment`
In your terminal: 
* `conda create -n test-env python=3.6`
* `conda activate test-env`
* conda [cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

### 5. Install needed packages`
Still in your terminal and in the root folder of your repository execute
* `pip install -r requirements.txt`

### 6. Make The Environment Visible in Jupyter Lab / Jupyter Notebook
In your terminal make sure the environment is activated and execute:
* `pip install ipykernel`
* `python -m ipykernel install --user --name <YOUR ENVIRONMENT> --display-name "<YOUR ENVIRONMENT DISPLAY NAME>"`

### 7. Start Jupyter Lab / Jupyter Notebook
* make sure the environment is activated
* just type `jupyter lab` or `jupyter notebook`
* **NOTE**: the folder, from which folder you started jupyter, will be your root folder. 


### 8. Install a Code Formatter
* it is a best-practice to format your Python code according to [PEP 8](https://www.python.org/dev/peps/pep-0008/)
* especially while learning, try to pay attention to it and correct yourself manually
* you can then automatically format your code by installing a code formatter
* make sure your environment is activated
* `pip install autopep8`
* `jupyter serverextension enable --py autopep8`


---


