## Using Laravel In A Docker Container

#### Requirements

- [docker](https://docker.com)
- docker-compose

##### Installation Instructions

Clone the git repo into your project. **Incase you want to create a microservice, all you need is to create a new project inside this repository and configure the container in the docker-compose.yml file**.

After you have cloned the repo, make sure your create a folder called storage in the root folder where src and config folders are.
repo > config > src > **storage** folder will come here > docker-compose.yml
Inside the storage folder, create three more folder **app**, **db** and **logs**. The naming doesn't matter as long as you change the docker-compose.yml file with the names you have given.

You can also use your terminal to create the folders as follows:

        ```
          > mkdir -p storage/app
          > mkdir -p storage/db
          > mkdir -p storage/logs

        ```

Once you have created the folders, open your terminal at the location of your folder and run **docker-compose up -d**

        ```
          myrepo> docker-compose up -d

        ```
