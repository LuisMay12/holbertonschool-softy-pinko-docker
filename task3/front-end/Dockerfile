FROM nginx:latest

# Copy the static site to the required path
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Replace the default site config
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Expose the port we'll use
EXPOSE 9000
