Use these Commandos (See: https://wiki.ubuntuusers.de/DNS-Server_Bind)

"sudo apt-get install bind9"
"sudo /etc/init.d/bind9 stop"
"nano /etc/bind/10.129.zone" 
"nano /etc/bind/db.fffl"
"sudo /etc/init.d/bind9 start"

In every Change of the Databases you MUST count up the "serial" and restart Bind with:
"service bind9 restart"


To Add these files to your dns server just setup Bind9 an add these two lines to yout /etc/bind/named.conf.local" files:

zone "fffl" {type master; file "/etc/bind/db.fffl"; };

zone "129.10.in-addr.arpa" {type master; file "/etc/bind/10.129.zone"; };

