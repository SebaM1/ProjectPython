                                                            ## End to End  Project ##

## Create Environment ##
    python -m venv venv1
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
    …or push an existing repository from the command line
    git remote add origin https://github.com/SebaM1/borrar.git
    git branch -M main
    git push -u origin main