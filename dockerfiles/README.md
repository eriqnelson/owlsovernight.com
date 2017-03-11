#H1 Dockerfile Builds
Dockerfiles contained in these directories will require their paths be passed on build and should be built from the project root.

1. firebase
2. gulp

##H2 firebase
docker build -f dockerfiles/firebase/Dockerfile -t owlsfirebase ./
##H2 gulp
docker build -f dockerfiles/gulp/Dockerfile -t owlsgulp ./
