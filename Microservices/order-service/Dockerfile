# Base image
FROM node:18-alpine
# Set working directory
WORKDIR /usr/src/app
# Copy dependency files
COPY package.json ./
COPY app.js ./
# Install dependencies
RUN npm install
# Expose service port
EXPOSE 3002
# Start the service
CMD ["npm", "start"]
