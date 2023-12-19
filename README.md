# 🚢 DB-Containers

A repository to help you in the creation of a database server with an administrator through phpmyadmin. In the future this repo will manage some types of db.

# Welcome 🚀
First of all, welcome, if you are here it's because I'm probably the one who is no longer there and you need this documentation to know how to maintain, modify and update the project. I want you to know that you can count on my total support.

I attach my networks in case you need to contact me:

- 📷 Instagram: [@rocketmx_](https://www.instagram.com/rocketmx_/)
- 🐙 GitHub: [@byNestorCode](https://github.com/byNestorCode/)

# ❓Requirements for the execution of the project:

1.  🐋 Docker and Docker-compose
    - Check the installation requirements for your operating system:
        - To install on 🐧 Linux: https://docs.docker.com/engine/install/ubuntu/
        - To install on 🪟 Windows: https://docs.docker.com/desktop/install/windows-install/
        - To install on 🍎 Mac: https://docs.docker.com/desktop/install/mac-install/

# 📄 (.env)Creation of environment variables

For the system to compile successfully we will need to configure the environment variables, but... What do you think? 😏

🤫***ARE SECRETS***🤫 and totaly customizable.

1. ☢️ Remove PORT in docker-compose.yml and add your custom port ej. '3306:3306'
2. ✍️ Create a .env file in the root of the project
3. 🌀 Add the next variables:
    - PMA_HOST=
    - UPLOAD_LIMIT=
    - *MYSQL_USER=
    - *MYSQL_PASSWORD=
    - MYSQL_ROOT_PASSWORD=
    *not required

# ❓❓ WTF is that?

Let's see the definitions:

- ***PMA_HOST***: define address/host name of the MySQL server. In this case 'db' because it's the name of mysql container.
- ***UPLOAD_LIMIT***: if set, this option will override the default value for apache and php-fpm (format as (0-9+)(K,M,G) default value is 2048K, this will change upload_max_filesize and post_max_size values).
- ***MYSQL_USER*** and ***MYSQL_PASSWORD***: These variables are optional, used in conjunction to create a new user and to set that user's password. This user will be granted superuser permissions (see above) for the database specified by the MYSQL_DATABASE variable. Both variables are required for a user to be created. Do note that there is no need to use this mechanism to create the root superuser, that user gets created by default with the password specified by the MYSQL_ROOT_PASSWORD variable.
- ***MYSQL_ROOT_PASSWORD***: (from user root) This variable is mandatory and specifies the password that will be set for the MySQL root superuser account. In the above example, it was set to my-secret-pw.

# 🐳 Once Docker is installed and 📄.env has been created:

1. We go to the root folder of the project, just where DockerFile and docker-compose.yml are located

2. Just execute the following command:

```bash
docker-compose up 
```

# ❗❗ IMPORTANT

If you have problems connecting to your bbdd, do not forget to use the ip of the bridge network of your docker service. The IP of your service is similar to the following:

```bash
172.xx.xx.1
```
