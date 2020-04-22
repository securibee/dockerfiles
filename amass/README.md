# Run Amass using Docker

## Prerequisites
1. [Install Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04) for your particular Operating System
2. Build the Docker image
```bash
docker build -t amass .
```
3. Profit


## Usage
Use [docker run]((https://docs.docker.com/engine/reference/run/)) to execute a command in your new container:
```bash
docker run -v OUTPUT_DIR_PATH:/.config/amass/ amass enum --list
```
Replace `OUTPUT_DIR_PATH` with the directory that contains your input files, e.g. `wordlist.txt`. Use `$(pwd)` for current directory.

For more information visit [Amass](https://github.com/OWASP/Amass/blob/master/doc/user_guide.md) and make sure to give them your support!