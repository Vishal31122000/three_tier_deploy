# Use a smaller base image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the application's dependencies inside the container
RUN npm install --only=prod

# Copy the rest of the application code to the container
COPY . .

# Expose Port to the container
EXPOSE 8080

# Specify the command to run when the container starts
CMD [ "node", "index.js" ]

