FROM node:latest as build 
# Set the working directory
WORKDIR /usr/src/app 
# Add the source code to app
COPY ./index.html /usr/share/nginx/html/index.html
# Install all the dependencies
RUN npm install 
# Generate the build of the application
RUN npm run build
# Stage 2: Serve app with nginx server 
# Use official nginx image as the base image
FROM nginx:latest 

# Copy the build output to replace the default nginx contents.
# COPY --from=build /usr/src/app/dist/growing-solution /usr/share/nginx/html

