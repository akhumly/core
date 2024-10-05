# Use a Node.js base image
FROM mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm

#Install NestJS CLI globally
RUN npm install -g @nestjs/cli

# Copy only package.json and package-lock.json to leverage Docker caching
COPY backend/package*.json ./backend

# Set the working directory 
#WORKDIR /backend

# Install dependencies
#RUN npm install

# Copy the rest of your application code to the container
# COPY . .

# Expose the NestJS default port (3000)
EXPOSE 3000

# Default command (overwritten by docker-compose command)
CMD ["npm", "run", "start:dev"]
