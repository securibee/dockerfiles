# Serve http files using Docker (nginx)

Full credit to Ronnie Flathers https://twitter.com/ropnop 

https://blog.ropnop.com/docker-for-pentesters/#example-5---serving-http-files

## Prerequisites
```
docker build .
```

## Usage
```
docker run --rm -it -p 80:80 -p 443:443 -v "${PWD}:/srv/data" nginxserve
```

## Useful

Make an alias for quick access
```
alias nginxhere='docker run --rm -it -p 80:80 -p 443:443 -v "${PWD}:/srv/data" nginxserve'
```
