# Use a Node 16 base image
FROM node:16-alpine 
# Set the working directory to /app inside the container
WORKDIR /app
# Copy app files
COPY . .
# ==== BUILD =====
# Install dependencies (npm ci makes sure the exact versions in the lockfile gets installed)
RUN npm install 
# Build the app
RUN npm run build
# ==== RUN =======
EXPOSE 3000
# Start the app
CMD [ "npm", "start" ]
