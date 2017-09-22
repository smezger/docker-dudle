dudle
==========
Setup your own dudle!

## Docker image content
1. Debian
1. Apache webserver
1. Dudle software from https://github.com/kellerben/dudle
1. CSS files from https://github.com/kellerben/dudle-css
1. Dudle config file
1. Accessible via proxy

## usage
### just run it
1. **docker run --name dudle -p 8888:80 -d jaydee2202/dudle**
1. **Create a reverse proxy that points to port 8888**
1. **Point your browser to that (sub)domain**
1. **Enjoy making you own polls**

### just build it
1. **clone repository**
1. **set it up like the config files, add css files etc.**
1. **build the container, e.g. docker build -t jaydee2202/dudle .**
1. **run the container with docker-compose up -d or docker run --name dudle -p 8888:80 -d jaydee2202/dudle**

## persistent polls
Unfortunately the software put the poll data in the webroot, so if you want to persist the polls,
you have to put the whole webroot (/var/www/html/dudle) on an external storage.
