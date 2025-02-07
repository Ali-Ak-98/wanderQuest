# Use official Node.js image as the base image
FROM node:18

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json (or yarn.lock) into the container
COPY package*.json ./

# Install the project dependencies
RUN npm install --production

# Copy the rest of the application code into the container
COPY . .

# Expose the port that NestJS will run on (default: 3000)
EXPOSE 3000

# Build the application (if needed, use ts-node for runtime if not built ahead)
RUN npm run build

# Start the app using the compiled JavaScript code
CMD ["npm", "run", "start:prod"]
