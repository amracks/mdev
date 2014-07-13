# CentOS-Based Android Development VM

## Requirements
* Vagrant
* librarian-puppet
* VirtualBox (if you use my vagrant box)

## Running
1. git clone https://github.com/amracks/mdev.git
2. cd mdev
3. librarian-puppet update
4. copy conf/user.yaml.example conf/user.yaml
5. edit conf/user.yaml
6. vagrant up

## What you get
* A 64bit CentOS VM running in GUI mode
* Android SDK installed in /opt
* Android SDK dependancies installed (openjdk, i686 glibc, etc.)
* Latest apache ant installed in /opt
