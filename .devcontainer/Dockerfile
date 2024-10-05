# Base image for Node.js development from devcontainers
FROM mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm

# Install NestJS CLI globally
RUN npm install -g @nestjs/cli

# Ensure the container uses the correct working directory
WORKDIR /workspaces/${localWorkspaceFolderBasename}

# Install project dependencies (including NestJS-specific packages)
COPY package*.json ./
RUN npm install

# Copy the rest of your application code into the container
COPY . .

# Expose the default NestJS port (if you plan to run it inside the container)
EXPOSE 3000

# Default command will be overridden by docker-compose.yml's 'command' if set.
CMD ["npm", "run", "start:dev"]
