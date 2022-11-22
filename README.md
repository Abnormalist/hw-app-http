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
In this repo the build process with git wark-flow to docker_registry
```
name: go application

on:
  push:
   branches: [ main ]
  pull_request:
    branches: [ main ]
      
jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v1
    - name: Build & Push Image
      run: |
        echo "${{ secrets.DOCKERPW }}" | docker login -u "4435561349" --password-stdin
        docker image build -t 4435561349/apptest:latest .
        docker push 4435561349/apptest:latest
```





