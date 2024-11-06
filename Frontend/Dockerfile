# Base image
FROM node:latest

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files to the container
COPY . .

# Expose the port used by Vite (5173 by default)
EXPOSE 5173

# Command to start the Vite development server in host mode
CMD ["npm", "run", "dev", "--", "--host"]

