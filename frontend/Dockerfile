FROM caddy:2-alpine

# Copy the HTML file to Caddy's default web root
COPY index.html /usr/share/caddy/

# Set the working directory to the web root
WORKDIR /usr/share/caddy

# Copy the Caddyfile configuration
COPY Caddyfile /etc/caddy/
ENV API_BASE="localhost"

# Expose port 8080 as specified
EXPOSE 8080

# Caddy will automatically use the Caddyfile and serve files from /usr/share/caddy/
# The templates directive in Caddyfile enables template processing for API_BASE variable
