FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code  
COPY . .

# Build the application
RUN npm run build

# Install serve to run the built app
RUN npm install -g serve

# Expose port 5173 (default Vite port)
EXPOSE 5173

# Start the application
CMD ["serve", "-s", "dist", "-l", "5173"]
