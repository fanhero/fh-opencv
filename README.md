# Heroku buildpack with openCV and python support

## What
This buildpack provides a self-contained environment for python applications that need:
OpenCV or Numpy.

## Why
Thumbor works best when all of its engines use openCV built with TBB support. This is a custom build which implements openCV 3.0.1 over the standard 2.x buildpacks. TBB support is enabled to give remoteCV the most "power".

## How
A complete environment was created using the Dockerfile file based on the heroku cedar stack v14.

This buildpack will download that environment and place it in your /app/.heroku folder.
This includes the following:
- Python-2.7.10
- Opencv-3.0.1 (with python support)
- Numpy-1.11.1


The buildpack is compiled with docker.
To compile the build run the `vendor.sh` file
`chmod a+x vendor.sh'
'./vendor.sh'



original Dockerfile forked from https://github.com/diogojc/heroku-buildpack-python-opencv-scipy
