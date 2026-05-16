# networking---change-hostname-ip-gateway-dns
heyyy , here are the command for change hostname , IP Addresses , Gateway and DNS . in Linux

change hostname :-
#hostname
#hostnamectl set-hostname server1.lab.example.com

ip 
#nmcli con show 
#nmcli con mod "System eth0" ipv4.addreses "172.25.250.11/24"       "/24 are netmask"

gateway
#nmcli con mod "System eth0" ipv4.gateway 172.254.250.25

dns
#nmcli con mod "System eth0" ipv4.dns 172.254.250.25         "gateway and dns are same for security"

to set all of the 
#nmcli con up "System eth0"
#ping -c3 172.25.250.11
#ping -c3 172.254.250.25
#reboot
