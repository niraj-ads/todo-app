# Use an official Node.js image as the base image
FROM node:20

# Set the working directory inside the container
WORKDIR /usr/src/app/

# Copy everything
COPY . .

# Delete the existing node_modules & build directory
RUN rm -rf node_modules build

# Synchronize package.json and package-lock.json
RUN npm install --package-lock-only

# Install the dependencies
RUN npm install

# Expose the port the app will run on
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]
