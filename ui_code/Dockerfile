# Use an official Node.js runtime as a parent image

FROM node:14-alpine

 

# Set the working directory to /app

WORKDIR /app

 

# Copy the package.json and package-lock.json files to the container

COPY package*.json ./

 

# Install app dependencies

RUN npm install

 

# Copy the rest of the application code to the container

COPY . .

 

# Build the React app

RUN npm run build

 

# Install the serve package to serve the built app

RUN npm install -g serve

 

# Set the environment variable to serve the app on port 3000

ENV PORT=3000

 

# Expose port 3000 for incoming traffic

EXPOSE 3000

 

# Set the default command to start the React app

CMD ["npm", "run", "serve"]

 





