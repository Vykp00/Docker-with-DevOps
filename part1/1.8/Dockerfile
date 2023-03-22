# Start from ubuntu:20.04 image
FROM ubuntu:20.04

# Install curl in this image
RUN apt-get update
RUN apt-get install -y gcc
RUN apt-get install -y curl

# Use /usr/src/app as workdir
WORKDIR /usr/src/app

# Copy the website.sh file from this location to workdir
COPY website.sh .

# Add execution permission during the build
RUN chmod +x website.sh

# When running docker run the command
CMD ./website.sh
