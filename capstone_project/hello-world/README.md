# Hello World

This is a simple react app. In order to run this locally follow the
instructions:

* Install node.js version `v16.13.1`
* Install the node.js dependencies `npm install`
* Run the application `npm start`
* Also you can run the tests by using `npm run test`
* To build a production app you can use `npm run build`

# Create React App Docker Image 🚀🐳

A brief description of what this project does

This repository contains a Docker image for running a basic Create React App.
Part of the Capstone Project From ITJuana DevOps Bootcamp

## Getting Started 🏁
#### Method One: Getting docker image from Docker-Hub 🐳

To get started, you'll need to have Docker installed on your machine. Once you have Docker installed, you can pull the image using the following command:

```sh
docker pull libradoz/itj-react-app:latest
```

After pulling the image, you can run it using the following command:
```sh
docker run -p 3000:3000 -d libradoz/itj-react-app
```

This will start the app in detached mode and make it available at `http://localhost:3000`.

#### Method Two: Building the Docker image using the dockerfile 🐳

You can build the image using the following command:

```sh
docker build -t libradoz/itj-react-app .
```

After building the image, you can run it using the following command:
```sh
docker run -p 3000:3000 -d libradoz/itj-react-app
```

This will start the app in detached mode and make it available at `http://localhost:3000`.

## Stopping the Container 📦

To stop the container, you can use the `docker stop` command followed by the container ID or name. You can find the container ID by running `docker ps`.

Here's an example of how to stop the container: 🚢
```sh
docker stop <container_id>
```

## Viewing Logs 📜

To view the logs of the container, you can use the `docker logs` command followed by the container ID or name. Here's an example of how to view the logs:
```sh
docker logs <container_id>
```