FROM node:latest
RUN npm install gulp-cli -g
RUN mkdir /owls
VOLUME /owls
WORKDIR /owls
RUN mkdir -p src/{html,images,js,scss} build/{html,images,js,css}
COPY /src /owls/src
COPY gulpfile.js /owls/src
COPY package.json /owls/src
RUN npm install gulp --save-dev
RUN npm install jshint gulp-jshint gulp-sass gulp-concat gulp-uglify gulp-rename --save-dev
CMD ["/bin/bash"]
