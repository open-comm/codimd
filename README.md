# Codimd Configuration

Ready to use codimd docker-compose configuration for a traefik web proxy.

CodiMd is an collaborative markdown editor.

* codimd repository: https://github.com/hackmdio/codimd


## Install

```
# clone repository
git clone https://git.open-communication.net/open-communication/docker/codimd.git

# move into the project folder
cd codimd

# copy and edit the environment configuration file
cp sample.env .env
```

Edit the `.env` file and change the following value:

* `DatabaseRootPassword` create a new safe password
* `DatabaseUserPassword` create a new safe password
* `your.codimd.domain` the domain name under which this codimd will be available


## Start & Stop Codimd

```
# start codimd
docker-compose up -d

# stop codimd
docker-compose down

# upgrade container
docker-compose pull
```

## Further  Customization

In order to be able to upload data you need to change the permissions of the folder `upload-data`.
Allow user named `hackmd` in the docker to access the volume, which user id and group id are `uid=1500`, `gid=1500`.
You can change the volume permission though this command: `chown -R 1500:1500 upload-data`.

For more information see codimd documentation:
https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-docker-deployment

