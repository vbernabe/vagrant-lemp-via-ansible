# Vagrant LEMP via Ansible Provisioning
This is a flexible setup that will handle projects running on LEMP using Ansible to provision and setup needed packages

Setup includes

  - [Ubuntu 14.04 (Trusty Tahr)]
  - [PHP 5]
  - [Nginx]
  - [MySQL]
  - [PHP5-Fpm]
  - [Mcrypt]
  - [Adminer]

## Pre-Requisite

User should already have

* [Virtualbox]
* [Vagrant] 
* [Ansible]

## Setup

Once you have the above pre-requisite installed you can follow the instructions below

Clone this repository
```sh
$ git clone https://github.com/vbernabe/vagrant-lemp-via-ansible.git vagrant-ansible
```

Create and provision your VM via Vagrant with Ansible
```sh
$ cd vagrant-ansible
$ vagrant up
```

Start your vagrant box
```sh
$ vagrant up
```

Try and access your web browser
```ssh
http://localhost:8080/
```

#### Done!

## Using your VM with your project

> Your vagrant-ansible dir will have a ***"projects"*** folder which will be the location of your DOCUMENT_ROOT.

***Projects*** folder currently have 2 files

* index.php - sample index file with phpinfo() you can
* adminer.php - this is similar to PHPMyAdmin to help you access MySQL

You can drop your source folder under ***"projects"*** folder and access via http://localhost:8080/yourprojectname

## Fine tune your VM 

If your project needs other dependencies or configuration you can ssh to your Vagrant Ubuntu VM and install any libraries needed.

```sh
$ vagrant ssh
```

### Credentials
* MySQL
    * Username: root
    * Password: empty
* VM - has sudo access
    * Username: vagrant
    * Password: vagrant


## Stopping VM
Stop your VM if not in used

Stop vagrant
```sh
$ vagrant halt
```

## Complete Cleanup

```sh
$ vagrant destroy
```

## Others
For Windows Users you need to install PuTTy to manage Vagrant

Other vagrant commands: https://www.vagrantup.com/docs/cli/

License
----

The MIT License (MIT)

Copyright (c) <2016>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [virtualbox]: <https://www.virtualbox.org/wiki/Downloads>
   [vagrant]: <https://www.vagrantup.com/downloads.html>
   [adminer]: <https://www.adminer.org/>
   [Ubuntu 14.04 (Trusty Tahr)]: <http://releases.ubuntu.com/14.04/>
   [PHP 5]: <http://php.net/>
   [PHP5-Fpm]: <https://php-fpm.org/>
   [MySQL]: <http://www.mysql.com/>
   [Nginx]: <https://www.nginx.com/>
   [Mcrypt]: <http://mcrypt.sourceforge.net/>
   [Ansible]: <http://docs.ansible.com/ansible/intro_installation.html>

