FROM node:latest
RUN mkdir /owls
WORKDIR /owls
VOLUME /owls
RUN mkdir -p src/{html,images,js,scss} build/{html,images,js,css}
COPY /src /owls/src
COPY gulpfile.js /owls
COPY package.json /owls
RUN npm install gulp-cli -g
RUN npm install --save-dev
# RUN npm install jshint gulp-jshint gulp-sass gulp-concat gulp-uglify gulp-rename --save-dev
EXPOSE 8080
RUN gulp
CMD ["/bin/bash/"]
# Nothing ever Works In Windows
s
