# Use the latest version of Ubuntu asa the base image
FROM ubuntu:22.04

# Update API and upgrade existing packages
RUN apt-get update
RUN apt-get upgrade -y

# Installs python3 and pip
RUN apt-get install -y python3 python3-pip

# Use pip3 to install Flask
RUN pip3 install flask

# Use pip3 to install Flak-cors
RUN pip3 install flask-cors

# Set working directory in the container
WORKDIR /app

# Copy the API file into the container
COPY api.py /app/api.py

# Expose port for flask
EXPOSE 5252

CMD ["python3", "/app/api.py"]

# How to build: docker build -t image1 .