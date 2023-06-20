# Dockerfile for building a container image for an Aesthisia demo app based on Node.js 16 runtime
# 
# This Dockerfile sets up an image for running a demo application called Aesthisia.
# The application is built on Node.js 16 runtime and can be run using npm package manager.


# Start with the official Node.js 16 image
FROM node:16

# Set the working directory inside the container
WORKDIR /React-js

# Copy the package.json file to the working directory
COPY package.json .

# Install neccessary  dependencies using npm package manager
RUN npm install

# Copy the application files to the working directory in the container
COPY . .

# Expose port 3000 to access app over browser
EXPOSE 3000

# Start the application when the container is started
CMD ["npm","start"]
