# Alfresco integration with ONLYOFFICE

This Alfresco Docker Compose template provides a simple configuration to test the integration with ONLYOFFICE available in  https://github.com/ONLYOFFICE/onlyoffice-alfresco. The project provides Alfresco addons for Repository and Share; this deployment applies both addons to Alfresco.

## Requirements

* Docker

## Using

Review the following line in [alfresco/alfresco-global.properties](alfresco/alfresco-global.properties) file...

```
onlyoffice.url=http://192.168.1.143/
```

... and replace `192.168.1.143` by your local IP. You can obtaint your local IP using `ifconfig` command or equivalent.

Once that is fixed, just start Docker Compose:

```
docker-compose up --build --force-recreate
```

Every document able to be used with *ONLYOFFICE* will include a new **Edit in ONLYOFFICE** action, that will open Collabora Online editing tool for the document as a new browser window. Once the document is closed in ONLYOFFICE, modifications will be updated in Alfresco in the background.

>> Note that many users can open the same document at the same time

In addition, for documents with formats that can be converted to *ONLYOFFICE* accepted formats, two new actions will be added to Alfresco Share Documents: **Read in ONLYOFFICE** (that opens the document in ONLYOFFICE using a new browser window) and **Convert using ONLYOFFICE** (that creates a new copy of the document in Alfresco Share that ONLYOFFICE is able to manage for editing purposes)


## Service URLs

http://localhost:8080/share

user: admin
password: admin


