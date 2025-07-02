# docker-discussion
Docker Setup Complete

# Creating a dockerfile, follow these steps
FROM: Specifies the base image.
COPY or ADD: Adds files from your host system into the image.
RUN: Executes commands in the image, such as installing software.
CMD or ENTRYPOINT: Defines the command that runs when the container starts.
EXPOSE: Specifies the port the container will listen on.

# Creating docker image
docker build -t "name" .

# port mapping first 5000- docker image port, 2nd one host application run port number
docker run -p 5000:5000 "name"

# tagging
docker tag docker-flask chayan141/docker-flask:version1

# pushing to docker hub
docker push chayan141/docker-flask:version1

# pull the image
docker pull chayan141/docker-flask:version1

# running the app
docker run -p 5000:5000 chayan141/docker-flask:version1