# light weight Base image
FROM node:21-alpine

# Working Directory 
WORKDIR /app

# Copy package.json for dependency installation 
COPY package.json ./

# Install dependencies 
RUN npm install

# Copy Rest of the application code
COPY . .

# Expose port 5173
EXPOSE 5173

# Default command to run the application 
CMD ["npm", "run", "dev", "--", "--host"]

