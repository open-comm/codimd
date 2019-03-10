Codimd Configuration
====================

Ready to use codimd docker-compose configuration for a traefik web proxy.

CodiMd is an collaborative markdown editor.

* codimd repository: https://github.com/hackmdio/codimd


Install
-------

```
# clone repository
git clone git@gitlab.wachter-jud.net:docker/codimd.git

# copy and edit the sample configuration file
cd codimd
cp docker-compose.yml.sample docker-compose.yml
```

Edit docker-compose.yml and change the following value:

* `DatabaseRootPassword` create a new safe password
* `DatabaseUserPassword` create a new safe password
* `your.codimd.domain` the domain name under which this codimd will be available




Usage
-----

```
# start codimd
docker-compose up -d

# stop codimd
docker-compose down

# upgrade container
docker-compose pull
```



