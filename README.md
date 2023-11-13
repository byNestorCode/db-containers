# 🚢 DB-Conteiners

a repository to help you in the creation of a database server with an administrator through phpmyadmin. In the future this repo will manage some types of db.

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
    - MYSQL_USER=
    - MYSQL_PASSWORD=
    - MYSQL_ROOT_PASSWORD=

# 🐳 Once Docker is installed and 📄.env has been created:

1. We go to the root folder of the project, just where DockerFile and docker-compose.yml are located

2. Just execute the following command:

```bash
docker-compose up 
```