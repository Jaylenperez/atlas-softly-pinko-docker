# Use the latest version of the Nginx image from Docker Hub
FROM nginx:latest

# Copy the front-end files from the local directory to the web server's root directory in the Docker image.
COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Copy the custom Nginx configuration file from the local directory to the Nginx configuration directory in the Docker image
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf