# Docker compose Magento2

This project sets up and environment for running Magento 2.
This will setup containers for NGINX, MySQl, PHP, a busybox container
used to hold the Magento 2 source code and two more busybox containers
to hold MySQL and NGINX configurations.

### Prerequisites

You should have docker engine and docker compose installed.
Read instructions [here](https://docs.docker.com/compose/install/)
on how to install them.

The NGINX container maps ports 5000 on the host to 80 on the container
and 5001 on the host to 443 on the container so make sure those
ports are available in the host.

### Instructions

1. Clone the repository and `cd` into the directory
2. Add your Magento 2 files to the src folder
3. Run `docker-compose up -d`

After it is done you should be able to access the Magento setup by going to
[http://localhost:5000/setup/index.php](http://localhost:5000/setup/index.php)

### MySQL credentials

* Username: magento
* Database: magento
* Password: pass123
