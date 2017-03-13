# Dockerfile Builds
Dockerfiles contained in these directories will require their paths be passed on build and should be built from the project root.

## Firebase
docker build -f dockerfiles/firebase/Dockerfile -t owlsfirebase ./
* Firebase will currently require authentication via CLI before each deployment. TODO: write ENV hooks into the Dockerfile
## Gulp
docker build -f dockerfiles/gulp/Dockerfile -t owlsgulp ./

* Gulp live reload server is configured to listen on port 8080 and should be mapped on run to an available host port.
