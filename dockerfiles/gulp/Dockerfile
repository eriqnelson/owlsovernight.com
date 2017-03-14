FROM ubuntu:latest
EXPOSE 80 8080 3000 35729
RUN apt-get update
RUN apt-get install curl -y
RUN apt-get install software-properties-common -y
RUN apt-get update
RUN apt-get install -y nodejs npm
# Debian installs `node` as `nodejs` so let's not do that
RUN update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10
RUN npm install --global gulp -y
RUN mkdir /owls
WORKDIR /owls
VOLUME /owls
RUN mkdir -p src/{html,images,js,scss} build/{html,images,js,css}
COPY /src /owls/src
COPY gulpfile.js /owls
COPY package.json /owls
RUN npm install --save-dev
# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
