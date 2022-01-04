# How to create a simple image in Docker
This simple project show you how to create a simple image of the project by docker commands.
## Installation
after installing Docker on your machine then follow this instructions:

<b>1. Clone the project</b>

<b>2. Open the powershell</b>

<b>3. Go to the project directory</b>

<b>4. Write this command:</b>

```bash
/> docker build -t hello-docker .
```

After that the image created and you can sure about that by this command:
```bash
/> docker images
```
<b>5. Then run the image by this command:</b>
```bash
/> docker run hello-docker
```
## Describe the Dockerfile
Any project that wants to be Dockerized needs this file.
```Docker
FROM node:alpine  
COPY . /app
WORKDIR /app
CMD node app.js

```
<b>FROM:</b> What container your project need to run or build
 
<b>COPY:</b> Copy all contents from root folder to 'app' folder in image's filesystem

<b>WORKDIR:</b> Go to 'app' directory for run commands

<b>CMD:</b> run the "node app.js" command


