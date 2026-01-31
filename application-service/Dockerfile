# Use official Node.js LTS image as the base
FROM node:18-alpine

# Set working directory inside container
WORKDIR /app

# Copy your index.js to the working directory
COPY index.js .

# Expose the port your app will listen on (adjust if needed)
EXPOSE 3000

# Command to run your Node.js app
CMD ["node", "index.js"]
