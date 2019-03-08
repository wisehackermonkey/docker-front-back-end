FROM node:10.0.0

# setup folders
RUN mkdir -p /server
WORKDIR /server

# include dependncy information
COPY . .
RUN npm install
