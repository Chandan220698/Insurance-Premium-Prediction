# Insurance Price Prediction

### Deployment Link:
[Insurance Price Prediction](https://insurance-premium-pred-ck.herokuapp.com/)

### Software and Accout Requirement.

1. [Github Account](https://github.com)
2. [Heroku Account](https://dashboard.heroku.com/login)
3. [VS Code](https://code.visualstudio.com/download)
4. [GIT CLI](https://git-scm.com/downloads)

### Steps
1. `git status`
2. `git add` 
3. `git commit -m "message"` Git commit create the version and push will push this changes to github
4. `git push origin main` This origin actually is the repo link
5. `git remote -v` To check repo link 

### Virtual environment and requirements.txt
1. Creating conda virtual env
`conda create -p <env_name> python==3.7 -y` -p to create venv in project folder itself
2. Activate venv
`conda activate <env_name>/`
or
`conda activate <env_name>`
3. Creating requirement.txt file
`pip freeze > requirements.txt`
4. To install requirements.txt
`pip install -r requirements.txt`

### To setpup CI/CD pipeline in heroku we need following information
1. HEROKU_EMAIL: kumarchndan07@gmail.com
2. HEROKU_API_KEY: <API_KEY>
3. HEROKU_APP_NAME: ml-deployment-project-ck

### BUILD DOCKER IMAGE
1. `docker build -t <image_name>:<tag_name> .`
> image_name should be in lower case and tag_name generally use 'latest'
2. `docker images` To list Docker Image and get IMAGE_ID
3. Run Docker Image
   `docker run -p 5000:5000 -e PORT=5000 <IMAGE_ID>`
4. `docker ps` To check running container in docker
5. `docker stop <container_id>` to stop docker container 


## Notes
> If adding '-e .' then we must have setup.py file in root directory. This will create <custom_pkg_name>-egg.info file for every package which contains "__init__.py" file.
> Where "-e ." executed inside "requirements.txt". Its actually lunching the "setup.py" hence the egg.info file will get created for all custom packages.