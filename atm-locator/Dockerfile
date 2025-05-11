# Copyright (c) 2023 Cisco Systems, Inc. and its affiliates All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

# Use Node.js 14 as the base image
FROM --platform=linux/amd64 node:14

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json into the working directory
COPY ./package*.json /usr/src/app/

# Install the project dependencies
RUN npm install

# Copy the rest of the application files into the container
COPY . ./

# Expose the application port (8001 in this case)
EXPOSE 8001

# Set the default command to run when the container starts
CMD ["npm", "start"]
