# Specify the base image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the rest of the app source code to the working directory
COPY . .

# Expose a port (if your app listens on a specific port)
EXPOSE 3000

# Define the command to run your app
CMD [ "npm", "start" ]
