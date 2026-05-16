# networking---change-hostname-ip-gateway-dns
heyyy , here are the command for change hostname , IP Addresses , Gateway and DNS . in Linux

change hostname :-                                                                                      <br>
#hostname                                                                                               <br>
#hostnamectl set-hostname server1.lab.example.com                                                       <br>

ip                                                                                                      <br>
#nmcli con show                                                                                         <br>
#nmcli con mod "System eth0" ipv4.addreses "172.25.250.11/24"                                           <br>

gateway                                                                                                 <br>
#nmcli con mod "System eth0" ipv4.gateway 172.254.250.25                                                <br>

dns                                                                                                     <br>
#nmcli con mod "System eth0" ipv4.dns 172.254.250.25                                                    <br>

to set all of the                                                                                       <br> 
#nmcli con up "System eth0"                                                                             <br>
#ping -c3 172.25.250.11                                                                                 <br>
#ping -c3 172.254.250.25                                                                                <br>
#reboot                                                                                                 <br>
