############################################################
# Dockerfile to build Flask app with Nginx and Gunicorn
############################################################

# Set the base image from https://hub.docker.com/_/python/
FROM python:3.6

# File Author / Maintainer
MAINTAINER Hossein Seyedmehdi (hossein.seyedmehdi@gmail.com)

# install application requirements
COPY requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

# Set the application working directory
WORKDIR /app

# Copy our code from the current folder to /app folder inside the container
ADD . /app

# Define our command to be run when launching the container
#CMD /bin/bash
CMD python /app/src/main.py