# Test App Go Service


#  <font color='red'>Requirements</font>
* Install on of the latest stable version of [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1), and install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* Install [Docker Compose](https://docs.docker.com/compose/install/#install-compose)

#  <font color='red'>Installation</font>
* Browse the repository's root
* Build the images 
    - `docker build -t hw-app-go`
* Start containers 
    - `docker run -d -p 11130:11130 --name app-go-hw

After starting containers you can test the Api at:
```url
http://localhost:11130/
```

#  <font color='red'>Code Building</font>
In this repo the build process with .github/workflows to docker_registry
It's up to you to fork and use it like you want.
After committing, you can find a docker image in the docker public registry



