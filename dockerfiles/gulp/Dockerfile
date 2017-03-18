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
RUN mkdir /app
VOLUME /app
COPY /app /app
COPY gulpfile.babel.js /app
COPY package.json /app
WORKDIR /app
# RUN npm install --save-dev babel-cli babel-preset-env
RUN npm install gulp
RUN npm install --save-dev
# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
