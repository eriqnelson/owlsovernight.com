FROM ubuntu:latest
EXPOSE 3000 3001
# 3000 for dev 3001 for dist
RUN apt-get update
RUN apt-get install -y nodejs npm
# Debian installs `node` as `nodejs` so let's not do that
RUN update-alternatives --install /usr/bin/node node /usr/bin/nodejs 10
RUN npm install --global gulp -y
RUN mkdir /app
VOLUME /app
COPY /app /app
COPY ["gulpfile.babel.js", "package.json", ".babelrc", "/app/"]
WORKDIR /app
# RUN npm install
# RUN npm install gulp
# RUN gulp
# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
# Cannot resolve why npm install works just fine when the image is attached but not from the Dockerfile command line
# All commands are commented out until I can resolve this
# For the moment run the following commands after RUN
# npm install
# gulp
# gulp serve
