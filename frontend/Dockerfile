# Use a smaller base image
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy only package.json and package-lock.json files to the container
COPY package*.json ./

# Install the application's dependencies inside the container
RUN npm install --production

# Copy the rest of the application code to the container
COPY . .

# Exposing Port to the container
EXPOSE 3000

# Specify the command to run when the container starts
CMD [ "npm", "start" ]

