# VPN

Bare Bones (PPTP) VPN Installer for CentOS

## Installation

To get started with your own secure VPN, simply execute the following commands at your servers command-line:

	$ yum install -y git
	$ cd /opt; git clone git://github.com/drewsymo/VPN.git
	$ cd bash install.sh

If you're on Linode, you can simply rebuild your instance with the `Pinch-installer` [stackscript](www.linode.com/stackscripts/).

## Features

* Installs a LEMP stack (PHP-FPM, MariaDB, APC, Nginx and Varnish Cache) via Yum
* Configures Varnish Cache with Nginx out-of-the-box
* Sets your hostname, timezone and installs essential tools
* Uses GoogleDNS with Level3 tertiary resolver
* Intelligentelly configures Nginx based on CPU cores
* Sets Varnish memory allocation percentage based on total memory
* Retrieves MariaDB server.cnf based on total memory
* Sets MariaDB root password and removes testing user / tables
* Creates a daily cron with email notifications for available Yum updates
* Secures your system via the following methods:
	* Creates privledged sudo user
	* Disable SSH root logins
	* Disables UseDNS
	* Change default SSH port
	* Enables SElinux
	* Firewall via iptables
	* Sets common network security parameters
	* Disables IPv6
	* Creates unprivledged www-data user for lemp components

## Author

**Drew Morris**

+ [Blog](http://drewsymo.com)
+ [Twitter](http://twitter.com/drewsymo)
+ [Google+](https://plus.google.com/u/0/114153589610660530694)