#### FROM
Specifies the base image for the Docker image.

```dockerfile
FROM image_name:tag

# Example
FROM ubuntu:20.04
```
#### WORKDIR
Sets the working directory for subsequent instructions.

```dockerfile
WORKDIR /path/to/directory

# Example
WORKDIR /app
```
#### COPY
Copies files or directories from the build context to the container.

```dockerfile
COPY host_source_path container_destination_path

# Example
COPY . .
```
#### RUN
Executes commands in the shell.

```dockerfile
RUN command1 && command2

# Example
RUN apt-get update && apt-get install -y curl
```
#### ENV
Sets environment variables in the image.

```dockerfile
ENV KEY=VALUE

# Example
ENV NODE_VERSION=14
```
#### EXPOSE
Informs Docker that the container listens on specified network ports at runtime.

```dockerfile
EXPOSE port

# Example
EXPOSE 8080

```
#### CMD
Provides default commands or parameters for an executing container.

```dockerfile
CMD ["executable","param1","param2"]

# Example
CMD ["npm", "start"]
```
or 
```dockerfile
CMD executable param1 param2
# Example
CMD npm run dev
```
#### ENTRYPOINT
Configures a container that will run as an executable.

```dockerfile
ENTRYPOINT ["executable","param1","param2"]

# Example
ENTRYPOINT ["node", "app.js"]
```
or
```dockerfile
ENTRYPOINT executable param1 param2

# Example
ENTRYPOINT node app.js
```
#### ARG

Defines variables that users can pass at build-time to the builder with the docker build command.
```dockerfile
ARG VARIABLE_NAME=default_value

# Example
ARG VERSION=latest
```
#### VOLUME
Creates a mount point for external volumes or other containers.

```dockerfile
VOLUME /path/to/volume

# Example
VOLUME /data
```
#### LABEL
Adds metadata to an image in the form of key-value pairs.

```dockerfile
LABEL key="value"

# Example
LABEL version="1.0" maintainer="Teja"
```
#### USER
Specifies the username or UID to use when running the image.

```dockerfile
USER user_name

# Example
USER app
```
#### ADD
Copies files or directories and can extract tarballs in the process.

```dockerfile
ADD source_path destination_path

# Example
ADD ./app.tar.gz /app
```
Similar to COPY, but with additional capabilities (e.g., extracting archives).

#### Example
```dockerfile
# Use an official Node.js runtime as a base image 
FROM node:20-alpine
# Set the working directory to /app 
WORKDIR /app
# Copy package.json and package-lock.json to the working directory
COPY package*.json ./
# Install dependencies 
RUN npm install
# Copy the current directory contents to the container at /app
COPY . .
# Expose port 8080 to the outside world 
EXPOSE 8080
# Define environment variable 
ENV NODE_ENV=production
# Run app.js when the container launches 
CMD node app.js
```