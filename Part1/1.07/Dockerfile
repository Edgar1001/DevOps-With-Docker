# Start from the alpine image 
FROM ubuntu:22.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Copy the server.sh file from this location to /usr/src/app/ creating /usr/src/app/server.sh
COPY server.sh .

# Update package list and install curl
RUN apt-get update && apt-get install -y curl
RUN chmod +x server.sh

# When running docker run the command will be ./server.sh
CMD ./server.sh

