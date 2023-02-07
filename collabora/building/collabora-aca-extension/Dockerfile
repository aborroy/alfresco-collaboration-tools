FROM node:10.22.1

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y default-jre-headless maven

RUN git clone https://github.com/CollaboraOnline/alfresco-collabora-online.git

WORKDIR /alfresco-collabora-online/collabora-aca-extension

RUN mvn clean package -DskipTests && mkdir /target

ENTRYPOINT cp -r /alfresco-collabora-online/collabora-aca-extension/target/*.tgz /target 
