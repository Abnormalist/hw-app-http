# Test App Go Service
Golang served by Nginx reverse proxy.


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
Golang is a compiled programming language so to make any changes to your app, you need to build the executable again.
In this repo the build process is done inside the docker-build process.
So when you need to re-compile the code you can follow this steps:


To simplify this steps you can create a makefile and group this commands in a single one, or on *nix system you can use this version of the commands: 
