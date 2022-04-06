FROM node:current-slim

LABEL MAINTAINER=vxchin@outlook.com

# Copy source code to /src inside container
COPY . /src

# Configure npm repository (in order to improve access speed in China)
RUN npm config set registry https://registry.npmmirror.com

# Install app and dependencies into /src inside container
RUN cd /src; npm install

# Document the port the app listens on
EXPOSE 8080

# Run this command (starts the app) when the container starts
CMD cd /src && node ./app.js
