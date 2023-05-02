# We need jdk8 I found this from Docker Hub
FROM openjdk:8

EXPOSE 8080

WORKDIR /usr/src/app

#Copy all files
COPY . .
#Install maven
RUN apt-get -o Acquire::Check-Valid-Until=false -o Acquire::Check-Date=false update -y &&\
    apt-get install maven -y

#Build a project
RUN mvn compile
RUN mvn package


# And finally the command to run the application
CMD ["java",  "-jar", "./target/docker-example-1.1.3.jar"]
