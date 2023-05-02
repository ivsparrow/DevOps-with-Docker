#Start from the ubuntu 20.04 image that is smaller but no fancy tools
FROM ubuntu:20.04

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
WORKDIR /usr/src/app

# Copy the curl.sh file from this location to /usr/src/app/ creating /usr/src/app/curl.sh
COPY curl.sh .

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.
RUN chmod +x curl.sh

# Execute a command to install curl
RUN apt-get -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false update -y &&\
    apt-get install curl -y

# When running docker run the command will be ./hello.sh
CMD ./curl.sh