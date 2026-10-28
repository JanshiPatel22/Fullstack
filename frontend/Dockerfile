
# Use Node.js 20 Alpine image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy frontend source code
COPY . .

# Build React application
RUN npm run build

# Install static file server
RUN npm install -g serve

# Expose frontend port
EXPOSE 80

# Serve the production build
CMD ["serve", "-s", "dist", "-l", "80"]
