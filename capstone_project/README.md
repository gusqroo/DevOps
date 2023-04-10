# DevOps Bootcamp Capstone Project
- [DevOps Bootcamp Capstone Project](#devops-bootcamp-capstone-project)
  - [Description](#description)
  - [Features and Requirements](#features-and-requirements)
  - [Guidelines](#guidelines)
  - [Resources](#resources)
  - [Pre-requisites](#pre-requisites)
  - [1. Setup your development environment](#1-setup-your-development-environment)
    - [Repository](#repository)
    - [Application](#application)
  - [2. Containerize the application](#2-containerize-the-application)
  - [3. Create a CI Pipeline](#3-create-a-ci-pipeline)
  - [4. Update "Hello World!" to "Hello DevOps!"](#4-update-hello-world-to-hello-devops)

## Description
In this project, you will be using some of the tools and technologies you have learned during the bootcamp.

## Features and Requirements
- Node Js application will be provided
- Containerization using docker
- CI pipeline using Github Actions (Including automated testing,build)
- Update the Node JS application content using Ansible

## Guidelines
- Instruction for the project will be available on Thursday, April 6th
- One week to deliver the project. Please deliver the project no later than Monday, April 17.
- Send the repo link or project to talent@itjuana.com
- After delivering the trainers will review the content, if you pass you’ll get a badge recognizing your knowledge as DevOps Engineer.
- You’ll know the results via email from the ITJ Talent Team.
- Any questions or comments, please post it in the [WhatsApp group](https://chat.whatsapp.com/KiirrKYAJ3SINrDn1pLZ7C)

## Resources
[Bootcamp Presentations](https://github.com/itjuana-bootcamp/DevOps/tree/main/Presentations)

## Pre-requisites

* [Docker](https://docs.docker.com/desktop/) installed
  * `docker --version` should show the docker version
* [Git](https://github.com/git-guides/install-git) installed
  * `git --version` should show the git version
* [Node JS](https://nodejs.org/en/download/package-manager/)
  * `npm version` should show the node version
* Have a [github account](https://github.com/join)
* Code editor of your preference - [VS Code](https://code.visualstudio.com/download) recommended

## 1. Setup your development environment

### Repository
- Go to the github repository https://github.com/itjuana-bootcamp/DevOps
- Fork the repository
NOTE: From here on, whenever we say repository , that refers to your forked repository.
- Clone the repository : `git clone git@github.com:<githubaccount>/DevOps.git`

### Application
- Go to folder `hello-world`
- Run `npm install` .
- Run `npm test` . All tests need to pass.
- Run `npm start` to run the application.
- Check http://localhost:3000 is reachable and displaying "Hello World!"

## 2. Containerize the application
- Using docker, containerize the application.
- Build the container and run it to make the application available on http://localhost:3000

## 3. Create a CI Pipeline 
- Create a CI pipeline which 
     - will trigger on push and on pull request
     - Run the tests
     - Only if tests are success, build the container

## 4. Update "Hello World!" to "Hello DevOps!"
- Update the node js application to display "Hello DevOps!" instead of "Hello World!" using ansible.



Capstone Resume 🚀
==================

-   There is two ways to controll the docker container:
    -   Using ansible in your local machine
    -   Using `Docker-compose` 

1\. Using ansible in your `local computer`
------------------------------------------

 - ### 1 - When running the container expose port 22:


```sh
  docker run -d -p 22:22 -p 3000:3000 libradoz/react-app
```

 - ### 2 - Make sure you have install `sshpass` on your local computer 💻

 - ### 3 - using your teminal go to the `ansible_files` directory

 - ### 4 - Make some changes to the ansible inventory.ini especify localhost and ansible_port it will look like this:
    
  ```[target1]
  localhost ansible_user=react-container ansible_password=12345 ansible_port=22
  ```
    
1\. Using ansible in your `local computer`
------------------------------------------
  - This project uses `docker-compose` 🐳 to set up and run two services: `hello-wolrd-app` and `ansible_controller`.

## Prerequisites 📋

  - To use this project, you'll need to have `docker-compose` 🐳 installed on your machine.

## Services 📦

### hello-wolrd-app 🌎💻
  - This is a container 🐳 hosting a basic React app created with `create-react-app`. It runs on port `3000`, so you can access it by going to `http://localhost:3000` in your web browser.

### ansible_controller 🤖🧠
  - This is a container 🐳 used as an Ansible controller. It has Ansible installed so we can perform changes to the `app.js` file when the Docker container hosting our app is running. This allows us to update the app without having to rebuild the Docker image.

## Usage 🔧

To use this project, you'll need to have `docker-compose` 🐳 installed on your machine.

1. Start the `docker-compose` by running the following command in one terminal:
```sh
docker compose up 
```

This will start both the `hello-wolrd-app` and `ansible_controller` services.

In a different terminal, access the `ansible_controller` container by running:

```sh
docker exec -w /home/ansible_controller/ansible_files/ -ti ansible_controller bash
```
This will open a bash shell inside the `ansible_controller` container.

Then, run the Ansible playbook with:
```sh
ansible-playbook -i inventory.ini playbook.yml
```
This will run the Ansible playbook and make changes to the `app.js` file in the `hello-wolrd-app` service.

👨‍💻 **Librado Hernandez** 💻 

- 📧 [Email](mailto:librado.cruzmx@gmail.com) - 🔗 [GitHub](https://github.com/libradito) - 💼 [LinkedIn](https://www.linkedin.com/in/librado-dev/)