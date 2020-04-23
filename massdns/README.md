# Run MassDNS using Docker

## Prerequisites
1. [Install Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04) for your particular Operating System
2. Build the Docker image
```bash
docker build -t massdns .
```
3. Profit


## Usage
Use [docker run]((https://docs.docker.com/engine/reference/run/)) to execute a command in your new container:
```bash
docker run -v $(pwd):/tmp/ massdns -r /tmp/resolvers.txt -t A -o J -w /tmp/massdnsresults.txt /tmp/domains.txt
```
Replace `$(pwd)` with the directory that contains your input files. Use `$(pwd)` for current directory.

For more information visit [MassDNS](https://github.com/blechschmidt/massdns) and make sure to give them your support!
