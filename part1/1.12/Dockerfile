# Install Node 16.x. From Docker Hub
FROM node:16

EXPOSE 5000

WORKDIR /usr/src/app

# Install all dependencies
COPY package*.json ./

# Copy source code 
COPY . .

# If I need the code for production
RUN npm ci --only=production

RUN npm install

# Build the static file
RUN npm run build

# Install serve
RUN npm install -g serve
 

# Finally, serve the project
ENTRYPOINT ["serve", "-s", "-l", "5000", "build"]
