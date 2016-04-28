# PhantomJS image

PhantomJS image built from sources (2.0.0) on Ubuntu 14.04.

This version also has Ruby 2.2.3 Installed on it too...

## Get the image

The image can be found in the MM docker registry (https://733578946173.dkr.ecr.eu-west-1.amazonaws.com/phantomjs2/).

```
mkdir -p docker-config
export DOCKER_CONFIG=$(pwd)/docker-config
set +x
eval $(aws ecr get-login)
set -x

docker pull 733578946173.dkr.ecr.eu-west-1.amazonaws.com/phantomjs2:latest
```
## Usage

You may run it on the command line:

```
docker run -t ≈ phantomjs --version
```

But you'll probably want to use it as a base image:

```
FROM 733578946173.dkr.ecr.eu-west-1.amazonaws.com/phantomjs2:latest
```

## Source

[Github Repository](https://github.com/mergermarket/docker-phantomjs)
