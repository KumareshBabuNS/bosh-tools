# PCF Ops Manager Tile Uploader

A script to upload tiles to a PCF Ops Manager from an Ops Manager ssh session.  
It is a simpler alternative to other tools such as [gng](https://github.com/mreider/gng).  

Steps to run it:

1. SSH into the Ops Manager VM (e.g. ```ssh <your-ops-manager-admin-id>@<opsmanager-hostname> ```)  

1. Copy [tileupload](https://raw.githubusercontent.com/pivotalservices/bosh-tools/master/tile-uploader/tileupload) file to the Ops Manager machine (e.g. ```git clone https://github.com/pivotalservices/bosh-tools.git ```)  

1. Edit ```tileupload``` and update the parameters below accordingly:  
```
   export OPS_MNGR_HOSTNAME=<your-ops-manager-host-name>   # do NOT include http/https or port number  
   export TILE_FILE_NAME=<tile-file-name>     # e.g. p-rabbitmq-1.6.4.pivotal  
   export PIVNET_TOKEN=<your-token-from-pivnet-profile>  
   export TILE_DOWNLOAD_URL=<tile-download-url-from-pivnet>  
   export OPS_MNGR_ADMIN_ID=<ops-mngr-admin-user-id>  
   export OPS_MNGR_PWD=<ops-mngr-admin-pwd>  
```
4. Run ```tileupload```

The tool will download the tile from the Pivotal Network website, get a token for the admin user and then upload the download tile to the Ops Manager blobstore using its API.
