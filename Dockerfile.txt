# Use the official Nginx image from Docker Hub
FROM nginx:alpine

# Copy your HTML files to the default Nginx directory
COPY ./html /usr/share/nginx/html

# Copy custom nginx configuration file if needed (optional)
# COPY ./nginx.conf /etc/nginx/nginx.conf

# Expose port 80
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
