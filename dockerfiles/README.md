# Dockerfile Builds
Dockerfiles contained in these directories will require their paths be passed on build and should be built from the project root.

## Firebase
docker build -f dockerfiles/firebase/Dockerfile -t owlsfirebase ./
## Gulp
docker build -f dockerfiles/gulp/Dockerfile -t owlsgulp ./
