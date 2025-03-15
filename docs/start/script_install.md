# Automated installation on an existing server using a shell script

There is a shell script in (``.homeinstall/hubzilla-setup.sh``) that will install Hubzilla and its dependencies on a fresh installation of Debian 9 stable (Stetch). It should work on similar Linux systems but your results may vary.

#### Requirements
The installation script was originally designed for a small hardware server behind your home router. However, it has been tested on several systems running Debian 9:

* Home-PC (Debian-9.2-amd64) and Rapberry-Pi 3 (Rasbian = Debian 9.3)

  * Internet connection and router at home
  * Mini-PC / Raspi connected to your router
  * USB drive for backups
  * Fresh installation of Debian on your mini-pc
  * Router with open ports 80 and 443 for your Debian

#### Overview of installation steps
1. `apt-get install git`
2. `mkdir -p /var/www/html`
3. `cd /var/www/html`
4. `git clone https://framagit.org/hubzilla/core.git .`
5. `nano .homeinstall/hubzilla-config.txt`
6. `cd .homeinstall/`
7. `./hubzilla-setup.sh`
8. `service apache2 reload`
9. Open your domain with a browser and step throught the initial configuration of $Projectname.


