FROM node:20-alpine
 
# Set the working directory inside the container
WORKDIR /app
 
# Copy package.json and package-lock.json
COPY package.json ./
# Install dependencies
RUN npm install -g webpack@$webpack_version webpack-cli
RUN yarn
 
# Copy the rest of your application files
COPY . .
 
# Expose the port your app runs on
EXPOSE 3002
 
# Define the command to run your app
CMD ["npm", "run", "dev"]