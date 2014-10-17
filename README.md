Precise-LAMP
============

A basic LAMP stack based on Ubunutu 14.04

Includes the basic LAMP Stack
(Apache2, MySQL and PHP)

* GIT
* Timezone = Europe/Berlin
* VIM
* XDebug
* and some more utils

Dependencies
============
To always keep your chef up to date this machine depends on the [vagrant-omnibus](https://github.com/opscode/vagrant-omnibus) plugin.

Install it via:
    $ vagrant plugin install vagrant-omnibus

Then you need to have the [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin for installing the right guest additions.

The installation is similar to the previous plugin:
    $ vagrant plugin install vagrant-vbguest

Finally you need to have the [vagrant-librarian-chef](https://github.com/jimmycuadra/vagrant-librarian-chef) plugin to get your recipes.

    $ vagrant plugin install vagrant-librarian-chef

For further details visit the plugin repositories linked in this document.



