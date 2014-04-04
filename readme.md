# LOOP Vagrant setup

## Vagrant setup
Install VirtualBox form [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

Install Vagrant from [http://www.vagrantup.com/downloads.html](http://www.vagrantup.com/downloads.html)

## Clone this repository

`git clone git@github.com:loopdk/vagrant.git`

## Vagrant add-ons
`vagrant plugin install vagrant-hostsupdater`

## First time
Make a folder named htdocs

`drush make --working-copy https://raw.github.com/loopdk/profile/development/drupal.make htdocs`

After bootstrap is done, connect to mysql and create a database for loop.

## Simple control of Vagrant
### To start
`vagrant up`

### To stop
`vagrant halt`

### To delete
`vagrant destroy`

## Information
Default IP: 192.168.50.11

Apache is available from [http://loop.vm](http://loop.vm)

Varnish from [http://loop.vm:8000](http://loop.vm:8000)

Solr [http://loop.vm:8983/solr](http://http://loop.vm:8983/solr)

Default mySQL password is 'vagrant'.

Remote x-debug is enalbed on port 9000 and connecting to 192.168.50.1
