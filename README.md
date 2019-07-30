## Using Laravel In A Docker Container

#### Requirements

- [docker](https://docker.com)
- docker-compose

##### Installation Instructions

Clone the git repo into your project. **Incase you want to create a microservice, all you need is to create a new project inside this repository and configure the container in the docker-compose.yml file**.

After you have cloned the repo, make sure your create a folder called storage in the root folder where src and config folders are.

```
repo > config > src > **storage** folder will come here > docker-compose.yml

```

Inside the storage folder, create three more folder **app**, **db** and **logs**. The naming doesn't matter as long as you change the docker-compose.yml file with the names you have given. You can change the following lines in the docker-compose.yml file.

```yml
  # web original file
  web:
    volumes:
      - ./src:/var/www
      - ./storage/app:/var/www/storage/app
      - ./storage/logs:/var/www/storage/logs
  # web new file
  web:
    volumes:
      - ./src:/var/www
      - ./storage/app_folder_name:/var/www/storage/app
      - ./storage/logs_folder_name:/var/www/storage/logs

  # db original file
  db:
    volumes:
      - ./storage/db:/var/lib/mysql

  # db new file
  db:
    volumes:
      # db will be changed to your app's mysql folder name in storage
      - ./storage/mysql_folder_name:/var/lib/mysql

```

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
