fai-config-space
================

Config space for Fully Automatic Installation (FAI).

This is the config that installs the mainserver. NOT FOR PRODUCTION USE, contains loads of ugly hacks!

Grab an .iso of it here: https://www.dropbox.com/s/9xyev3vv56ovpdb/sverigelinux-0.0.8-alpha.iso?dl=0

SverigeLinux is a deployment system for Linux servers and clients. It is based on Thomas Langes Fully Automatic Installation (FAI) and Debian-LAN by Andi Mundt et al. 
It has fully implemented LDAP+Kerberos authentication.

Howto:
======

Boot the image off a CD (USB install might not work) or run it in a VM. The harddisk of the machine/VM will be WIPED OF ALL DATA!

Go to https://ip-address/ to get to the fancy homepage. Implemented services are 
* FusionDirectory for LDAP-management, (login with "admin" + password)
* OwnCloud for storage,
* CUPS for printer management
* Icinga and Munin for system monitoring
* Bind for DNS
* isc-dhcp-server for DHCP (on by default)
* FAI for system deployment
* OpenLDAP + Kerberos

Known issues:
=============

* When choosing between STANDARD and SPECIAL, choose SPECIAL to specify IP address and subnetmask. When choosing, press the space bar, not Enter.

* After specifying admin password, the process might seem to halt. Have patience.

* The home-directory is not the same as the owncloud directory.

* Lots of ugly hacks for MySQL-database setup which makes this version very insecure and not suited for production use. This is a proof-of-concept and will be refined at a later stage.

Roadmap:
========

* Puppet classes for configuration management

* DNS management in LDAP

* DHCP management in LDAP
