# Use Node.js 20 as the base image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Create uploads directory for image storage
RUN mkdir -p uploads

# Expose the port (matches index.js default of 8000)
EXPOSE 8000

# Start the app
CMD ["npm", "run", "start"]