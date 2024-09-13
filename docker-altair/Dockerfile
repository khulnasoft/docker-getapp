FROM node:18.20.4-alpine AS build

# Build argument for NPM token
ARG NPM_TOKEN
ENV NPM_TOKEN=${NPM_TOKEN}

WORKDIR /app

# Copy .npmrc and package files
COPY ./app/.npmrc /app/.npmrc
COPY ./app/package.json /app/package.json
COPY ./app/package-lock.json /app/package-lock.json

# Install dependencies and remove .npmrc
RUN npm install --production && rm -f /app/.npmrc

FROM node:18.20.4-alpine AS final

WORKDIR /app

# Copy node_modules and the rest of the app from the build stage
COPY --from=build /app/node_modules /app/node_modules
COPY ./app /app

EXPOSE 3000

# Start the application
ENTRYPOINT ["npm", "start"]
