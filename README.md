To Add these files to your dns server just setup Bind9 an add these two lines to yout /etc/bind/named.conf.local" files:

"sudo apt-get install bind9"

"sudo /etc/init.d/bind9 stop"


zone "fffl" {type master; file "/etc/bind/db.fffl"; };

zone "129.10.in-addr.arpa" {type master; file "/etc/bind/10.129.zone"; };

