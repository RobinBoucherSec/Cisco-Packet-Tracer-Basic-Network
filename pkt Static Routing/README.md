faire un model qui se repete et est assez quick, TP6, 7, 7.1.2.3.4
and add pkt file independently


Static routing (do it in the CLI of each router and earase # Gatineau and all) will pass throught in block

Configuration des routes statiques (en console)

make sur you do 
en
config t
and past the ip route without the #ville

and each router of campus's

🔁 Routeur Montréal
ip route 192.168.1.64 255.255.255.224 172.16.1.2 # Gatineau
ip route 192.168.1.96 255.255.255.224 172.16.1.2 # Québec
ip route 192.168.1.128 255.255.255.224 172.16.1.2 # Ottawa
ip route 192.168.1.160 255.255.255.224 172.16.1.2 # Direction Générale

ip route 192.168.1.64 255.255.255.224 172.16.1.2
ip route 192.168.1.96 255.255.255.224 172.16.1.2
ip route 192.168.1.128 255.255.255.224 172.16.1.2
ip route 192.168.1.160 255.255.255.224 172.16.1.2

🔁 Routeur Québec
ip route 192.168.1.32 255.255.255.224 172.16.2.2 # Montréal
ip route 192.168.1.64 255.255.255.224 172.16.2.2 # Gatineau
ip route 192.168.1.128 255.255.255.224 172.16.2.2 # Ottawa
ip route 192.168.1.160 255.255.255.224 172.16.2.2 # Direction Générale

ip route 192.168.1.32 255.255.255.224 172.16.2.2
ip route 192.168.1.64 255.255.255.224 172.16.2.2
ip route 192.168.1.128 255.255.255.224 172.16.2.2
ip route 192.168.1.160 255.255.255.224 172.16.2.2


🔁 Routeur Ottawa
ip route 192.168.1.32 255.255.255.224 172.16.4.2 # Montréal
ip route 192.168.1.64 255.255.255.224 172.16.4.2 # Gatineau
ip route 192.168.1.96 255.255.255.224 172.16.4.2 # Québec
ip route 192.168.1.160 255.255.255.224 172.16.4.2 # Direction Générale

ip route 192.168.1.32 255.255.255.224 172.16.4.2
ip route 192.168.1.64 255.255.255.224 172.16.4.2
ip route 192.168.1.96 255.255.255.224 172.16.4.2
ip route 192.168.1.160 255.255.255.224 172.16.4.2

🔁 Routeur Gatineau
ip route 192.168.1.32 255.255.255.224 172.16.3.2 # Montréal
ip route 192.168.1.96 255.255.255.224 172.16.3.2 # Québec
ip route 192.168.1.128 255.255.255.224 172.16.3.2 # Ottawa
ip route 192.168.1.160 255.255.255.224 172.16.3.2 # Direction Générale

ip route 192.168.1.32 255.255.255.224 172.16.3.2
ip route 192.168.1.96 255.255.255.224 172.16.3.2
ip route 192.168.1.128 255.255.255.224 172.16.3.2
ip route 192.168.1.160 255.255.255.224 172.16.3.2

🔁 Routeur Direction Générale
ip route 192.168.1.32 255.255.255.224 172.16.1.1 # Montréal
ip route 192.168.1.64 255.255.255.224 172.16.3.1 # Gatineau
ip route 192.168.1.96 255.255.255.224 172.16.2.1 # Québec
ip route 192.168.1.128 255.255.255.224 172.16.4.1 # Ottawa

ip route 192.168.1.32 255.255.255.224 172.16.1.1
ip route 192.168.1.64 255.255.255.224 172.16.3.1
ip route 192.168.1.96 255.255.255.224 172.16.2.1
ip route 192.168.1.128 255.255.255.224 172.16.4.1



