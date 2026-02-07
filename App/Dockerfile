# Use Node.js 18 alpine for a small image size
FROM node:18-alpine

# Set the working directory
WORKDIR /usr/src/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install --production

# Copy the rest of your application code
COPY . .

# Your app.js uses process.env.PORT || 3001
# Render will automatically inject a PORT variable
EXPOSE 3001

# Command to run the application
CMD ["node", "app.js"]