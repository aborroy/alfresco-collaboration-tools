# Alfresco integration with Collabora Online

This Alfresco Docker Compose template provides a simple configuration to test the integration with Collabora Online available in https://github.com/CollaboraOnline/alfresco-collabora-online. Despite the `alfresco-collabora-online` project provides Alfresco addons for Repository, Share and ACA; this deployment only applies the addons for Repository and Share.

## Requirements

* Docker

## Using

Review the following lines in [docker-compose.yml](docker-compose.yml) file...

```
  -Dcollabora.public.url=http://192.168.1.143:9980/ 
  -Dalfresco.public.url=http://192.168.1.143:8080/alfresco/
```

... and replace `192.168.1.143` by your local IP. You can obtaint your local IP using `ifconfig` command or equivalent.

Once that is fixed, just start Docker Compose:

```
docker-compose up --build --force-recreate
```

Every document able to be used with *Collabora Online* will include a new **Edit in Collabora Online** action, that will open Collabora Online editing tool for the document as an *iFrame* inside Alfresco Share App.

>> Note that many users can open the same document at the same time


## Service URLs

http://192.168.1.143:8080/share (use your local IP instead of `192.168.1.143`)

user: admin
password: admin


