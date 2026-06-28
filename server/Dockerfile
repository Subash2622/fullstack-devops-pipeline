# Step 1 - Base Image
FROM node:24

# Step 2 - Create working directory
WORKDIR /app

# Step 3 - Copy package files
COPY package*.json ./

# Step 4 - Install dependencies
RUN npm install

# Step 5 - Copy application source code
COPY . .

# Step 6 - Expose application port
EXPOSE 5000

# Step 7 - Start the application
CMD ["npm", "start"]