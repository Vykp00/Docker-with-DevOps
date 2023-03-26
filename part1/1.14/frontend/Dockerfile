# Install Node 16.x. From Docker Hub
FROM node:16-alpine

EXPOSE 5000

WORKDIR /usr/src/app

# Install all dependencies
# Copy source code
COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm install

# Build the static file
RUN npm run build

# Install serve
RUN npm install -g serve


# Finally, serve the project
ENTRYPOINT ["serve", "-s", "-l", "5000", "build"]
