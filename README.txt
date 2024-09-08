                                                             ## End to End  Project ##


###### Enviroment and Repository #######
## Create Environment ##
    #create
    python -m venv venv1
    #activate
    venv1\Scripts\activate


## Conecction with GitHub Repository ##
    …or create a new repository on the command line
    echo "# borrar" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git branch -M main
    git remote add origin https://github.com/SebaM1/borrar.git
    git push -u origin main

## Para actualizar mi Git ## 
    git init
    git add .
    git commit -m "Agregando todos los archivos del proyecto"
    git push origin main
    git push -u origin main


    …or push an existing repository from the command line
    git remote add origin https://github.com/SebaM1/borrar.git
    git branch -M main
    git push -u origin main

## Name and Adress ## 
    git config --global user.name "SebaM1"
    git config --global user.email sebastian.molina@mi.unc.edu.ar

## .gitignore ##
    create file .gitignore in GitHub repository (Select python)
    gitpull

####### Setup.py #######

from setuptools import find_packages,setup
from typing import List

HYPEN_E_DOT='-e .'
def get_requirements(file_path:str)->List[str]:
    '''
    this function will return the list of requirements
    '''
    requirements=[]
    with open(file_path) as file_obj:
        requirements=file_obj.readlines()
        requirements=[req.replace("\n","") for req in requirements]

        if HYPEN_E_DOT in requirements:
            requirements.remove(HYPEN_E_DOT)
    
    return requirements

setup(
name='mlproject',
version='0.0.1',
author='SebaM1',
author_email='sebastian.molina@mi.unc.edu.ar',
packages=find_packages(),
install_requires=get_requirements('requirements.txt')

)
## Create requirements.txt
pandas
numpy
seaborn
-e .

##### In terminal #######
pip install -r requirements.txt
(se crea carpta mlproject.egg-info)

##### Create src folder #####
##  inside we create the folders=
        'Components'
        (data_ingestion, data_transformation, 
        model_trainer and __init__) 
    
        'pipeline'
        (predict_pipeline, train_pipeline
        and __init__)
    
    
    and 4 .py files 
    'exception.py', 'logger.py', 'utils.py'
    and '__init__.py'