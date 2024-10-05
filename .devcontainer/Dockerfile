# Use a Node.js base image
FROM mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm

# Set the working directory to the 'backend' folder
WORKDIR /workspaces/${localWorkspaceFolderBasename}/backend

# Copy only package.json and package-lock.json to leverage Docker caching
COPY backend/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of your application code to the container
COPY backend/ .

# Expose the NestJS default port (3000)
EXPOSE 3000

# Default command (overwritten by docker-compose command)
CMD ["npm", "run", "start:dev"]
