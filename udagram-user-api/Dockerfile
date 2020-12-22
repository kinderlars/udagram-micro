# Base Image NodeJS
FROM node:13

# Create workdir /usr/src/app
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy source folder to app source
COPY . .

# Bind the port that the image will run on
EXPOSE 8080

# Define the Docker image's behavior at runtime
CMD [ "npm", "run", "prod" ]