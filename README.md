# dshield

DShield Raspberry Pi Sensor

  This is a set of scripts to setup a Raspberry Pi as a DShield Sensor.
In order to use the Raspberry Pi, you will need to first prepare it:

- CHANGE THE DEFAULT SSH PASSWORD (better: use keys to authenticate)
- expose the Pi to inbound traffic. For example, in many firewalls
  you will be able to configure it as a "DMZ Hosts"

only on "Jessie Lite": sudo apt-get install git

git clone https://github.com/DShield-ISC/dshield.git

sudo dshield/bin/install.sh

  This script will:

- enable firewall logging and submitting of logs to DShield
- change your ssh server to listen on port 12222
- install the ssh honeypot cowrie (TODO)
- configure a default web server and submit logs to DShield (TODO)

Updates:

inside your "dshield" directory (the directory created above when you run "git clone"), run

git pull
then run the install script again (sudo bin/install)