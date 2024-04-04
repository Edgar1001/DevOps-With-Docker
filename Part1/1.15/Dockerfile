FROM golang:1.16-alpine

# Install necessary packages
RUN apk update && \
    apk add --no-cache git nodejs npm

# Clone the repository
RUN git clone https://github.com/Edgar1001/Timestamp-App.git /Timestamp-App

# Set the working directory
WORKDIR /Timestamp-App

# Copy package.json to the Docker build context
COPY package.json .

# Install npm dependencies
RUN npm install

# Expose port 8080
EXPOSE 8080

# Start the application
CMD ["npm", "start"]

