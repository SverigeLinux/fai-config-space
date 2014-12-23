fai-config-space
================

Config space for Fully Automatic Installation (FAI).

This is the config that installs the mainserver. 

Grab an .iso of it here: https://www.dropbox.com/s/yvcapxj3aaedzsm/sverigelinux-0.0.1-prealpha.iso?dl=0

SverigeLinux is a deployment system for Linux servers and clients. It is based on Thomas Langes Fully Automatic Installation (FAI) and Debian-LAN by Andi Mundt et al. 
It has fully implemented LDAP+Kerberos authentication.

Known issues:
=============

* When choosing between STANDARD and SPECIAL, choose SPECIAL to specify IP address and subnetmask. When choosing, press the space bar, not Enter.

* After specifying admin password, the process might seem to halt. Have patience.

* In this pre-alpha version, there is no possibility to choose domain and LDAP-domain. This functionality is developed but not yet implemented in the master branch.


Roadmap:
========

* Puppet classes for configuration management

* DNS management in LDAP

* DHCP management in LDAP
