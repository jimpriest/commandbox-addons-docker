# Ortus CommandBox + Adobe CF2018 Addons in Docker

This is an example of using the CommandBox Docker image along with Adobe's Addons Docker image to allow use of cfhtmltopdf. 

## Setup

First build: docker-compose build --no-cache

This will run Dockerfile which will copy the updated .prikey to the CommandBox image. 
The .prikey is used by ColdFusion to authenticate the PDFg engine.
Apparently some CommandBox images have the wrong key.


## Running 

docker-compose up

App: http://localhost/

CFAdmin: http://localhost/CFIDE/administrator

CFAdmin login is admin / password.


## Notes

The "profile": "development" in server.json allows access to CFAdmin.

See the myconfig.json used by CFConfig to configure the server and in particular the PDFServiceManagers section.

Thanks to @dbelanger (David Belanger) on CFML Slack for sharing the .prikey information and updated file.
Thanks to @Ryan on CFML Slack for pointing out the PDFServiceManagers options in CFConfig.


