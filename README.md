<h1 align="center">Welcome to Docker Init 👋</h1>
<p>
  <a href="https://github.com/nour-karoui/docker-init#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/nour-karoui/docker-init/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/nour-karoui/docker-init/blob/master/LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/github/license/bishkou/password-pwnd" />
  </a>
</p>

#### a simple react application to get started with docker and DevOps basics


### 🏠 [Homepage](https://github.com/nour-karoui/docker-init)


## Install

```sh
> git clone https://github.com/nour-karoui/docker-init.git
> cd frontend
// running the project locally
> npm i
> npm start
```

## How It Works

In this project, we prepared two dockerfiles, to **build two docker images**, one appropriate for **dev env** and the other one for **prod env**

To run this project, make sure you have docker installed and create an account on [Dockerhub](https://hub.docker.com/)

***PS***: You won't need any other dependencies installed, not even nodejs. Since the project on a container.
<hr />

### 1- Dev Environment

Dockerfile-dev builds an image for developing

##### Running The project
````shell script
docker build -t YOUR_DOCKER_ID/docker-react -f Dockerfile-dev .
docker run -p 3000:3000 YOUR_DOCKER_ID/docker-react
````

##### Running Tests

```shell script
docker run YOUR_DOCKER_ID/docker-react npm run test
```
<hr />
Since building a docker image means taking a snapshot of the current source code, later changes won't be detected in the docker container.
We configured the docker compose file so that local changes will be automatically propagated to the docker container.

&nbsp;

**So instead of**
```shell script
docker run -p 3000:3000 YOUR_DOCKER_ID/docker-react
``` 
**We simply write**
```shell script
docker-compose up
``` 

<hr />

### 2- Prod Environment
Dockerfile builds an image for production

````shell script
docker build -t YOUR_DOCKER_ID/docker-react-prod .
docker run YOUR_DOCKER_ID/docker-react-prod
````


<hr />

### 3- Github & Travis CI
Each time we push our code to the github repo, Travis CI is triggered to run the build a docker image and run the container to execute the tests and make sure everything works properly.

<hr />

## Author

👤 **Nour**

* Github: [@nour-karoui](https://github.com/nour-karoui)
* LinkedIn: [@nourkaroui](https://www.linkedin.com/in/nourkaroui/)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/nour-karoui/docker-init/issues). You can also take a look at the [contributing guide](https://github.com/nour-karoui/docker-init/blob/master/CONTRIBUTING.md).

## Show your support

Give a [STAR](https://github.com/nour-karoui/docker-init) if this project helped you!

## 📝 License

* Copyright © 2021 [Nour](https://github.com/nour-karoui).
* This project is [MIT](https://github.com/nour-karoui/docker-init/blob/master/LICENSE) licensed.

***
_This README was generated with by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
