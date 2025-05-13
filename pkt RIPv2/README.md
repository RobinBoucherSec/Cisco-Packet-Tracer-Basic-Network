## Static configurations

### 📝 Description

Here I do the configuration of RIVv2 for every vlan.

### 🎯 Objectives

With RIPv2 configurations, I want to be able to ping every devices togeter, regardless of their vlan.

### ⚙️ Steps Taken

When i open the CLI of any router, I start with the `cisco` password if needed and:
```
en
config t
```

Then, on each router of each campus's I do the following:
- 🔁 Routeur Montréal
```router rip
version 2
no auto-summary
network 172.16.1.0
network 192.168.1.32
```
- 🔁 Routeur Québec
```router rip
version 2
no auto-summary
network 172.16.2.0
network 192.168.1.96
```
- 🔁 Routeur Gatineau
```router rip
version 2
no auto-summary
network 172.16.3.0
network 192.168.1.64
```
- 🔁 Routeur Ottawa
```router rip
version 2
no auto-summary
network 172.16.4.0
network 192.168.1.128
```
- 🔁 Routeur Direction Générale
```router rip
version 2
no auto-summary
network 172.16.0.0
network 192.168.1.160
```



## Here are the tests of validation:


Vérifications (tests) à effectuer
Test Commande Résultat attendu
Vérifier la table de
routage
show ip route Routes RIP (code R) visibles
Ping entre clients ping IP-client-distant Réponse OK
Ping vers serveur DNS ping 192.168.1.161 Réponse OK
DNS lookup nslookup
web.cumberland... Adresse IP résolue
Web & FTP Navigateur / ftp Connexion aux services
centralisés OK




## Problem encountered


  ## 🔙 Back to Portfolio
[⬅️ Back to my Cybersecurity Portfolio](https://github.com/RobinBoucherSec/RobinBoucherSec)


