# Build James
#
# VERSION	1.0

FROM java:openjdk-8-jdk

# Install Maven
WORKDIR /root
RUN wget http://mirrors.ircam.fr/pub/apache/maven/maven-3/3.5.0/binaries/apache-maven-3.5.0-bin.tar.gz
RUN tar -xvf apache-maven-3.5.0-bin.tar.gz
RUN ln -s /root/apache-maven-3.5.0/bin/mvn /usr/bin/mvn

# Install git
RUN apt-get update
RUN apt-get install -y git

# Copy the script
COPY compile.sh /root/compile.sh

# Define the entrypoint
WORKDIR /james-project
ENTRYPOINT ["/root/compile.sh"]
