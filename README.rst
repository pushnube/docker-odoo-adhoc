Odoo Docker Compose and Images
==============================
Este repositorio contiene un conjunto de archivos docker para construir diferentes imágenes acoplables usadas por ADHOC.
También proporciona un archivo docker-compose para usar odoo de una manera simple.

La imagen predeterminada de odoo docker (adhoc / odoo-ar) que se usa en compose incluye muchos repositorios (y sus dependencias) generalmente utilizados por adhoc (principalmente repositorios de oca e ingadhoc)

Requirements
============

To use this docker compose file need:

* install pip "sudo apt-get install python-pip"
* docker-compose "sudo pip install --upgrade docker-compose"
* docker-engine "sudo curl -sSL https://get.docker.com/ | sh"
* we also recommend this so you can use docker without sudo

    * sudo groupadd docker
    * sudo gpasswd -a $USER docker
    * sudo service docker restart && newgrp docker
* clone this repository "git clone git@github.com:ingadhoc/docker-odoo-adhoc.git" (or "git clone https://github.com/ingadhoc/docker-odoo-adhoc.git")
* If you want to have areoo docs convertion you shoud run only once "docker run --name="aeroo" --restart=always -d adhoc/aeroo-docs"


Run and usefull commands
========================

* Run "docker-compose up"
* Odoo should be ready to be used on http://localhost:8069/
* Check .env for choosing odoo version and other useful configurations
* Remove everything (containers and data) "docker-compose down -v"

Links
=====
* `TODO: Using for production  <docs/developers_guide.rst/>`_
* `Tips and trics <docs/tips_and_trics.rst/>`_
* `Developers Guide <docs/developers_guide.rst/>`_
* `Images readme <dockerfiles/README.rst/>`_
* `Roadmap / Known Issues <docs/TODO.rst/>`_
* `Inspired by <docs/inspired_by.rst/>`_
