# DOCKERFILE:
# code to build your docker image and ultimately run your app as a container

# FROM - specifies the base(parent) image
# (such as openjdk, openjre, node etc.)

# WORKDIR - sets the working directory for the instructions that follow.

# COPY - copies files and directories to the container.

# RUN - runs a Linux command. Used to install packages into container
# (such as creating folders etc.)

# CMD - provides a command and arguments for an executing container
# (There can be only one CMD)

# ENV - sets environment variable. We can have multiple variables
# (environment variable which is passed to the container) 

# EXPOSE - expose ports
# (maybe you want to use something other than default localhost)

# ENTRYPOINT - provides command and arguments for an executing container
# (similar to CMD)

# VOLUME - mechanism for persisting data generated by container

# LABEL - key-value pairs that add custom metadata to your Docker Images.
# (maybe you want to organize images better)

# ADD - Copies files and directories to the container
# (Can also unpack compressed files)

# ARG - Define build-time variable
# (maybe you want to define a parameter and its default value)

# define the image we want to build from
FROM node:16

# create a workdir to hold the application code inside the image
WORKDIR /app

# add our dependencies to our container
COPY package.json ./

# run a linux command to install the app's dependencies 
RUN npm install

# copy over all files in local to the /app directory
COPY . .

# only one command allowed with the given arguments
CMD ["npm", "start"]