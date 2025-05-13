
## Static configurations

### 📝 Description

Here I do the configuration of static routing for every vlan.

### 🎯 Objectives

I want to be able to ping every devices togeter, regardless of their vlan.

### ⚙️ Steps Taken

When i open the CLI of any router, I start with the `cisco` password if needed and:
```
en
config t
```

Then, on each router of each campus's I do the following:


🔁 Routeur Montréal

- The **# City** indicate what it connects but I only need to enter the next code in the CLI.

ip route 192.168.1.64 255.255.255.224 172.16.1.2 # Gatineau

ip route 192.168.1.96 255.255.255.224 172.16.1.2 # Québec

ip route 192.168.1.128 255.255.255.224 172.16.1.2 # Ottawa

ip route 192.168.1.160 255.255.255.224 172.16.1.2 # Direction Générale

- I add to ths CLI of the Montréal Router with this:

```
ip route 192.168.1.64 255.255.255.224 172.16.1.2

ip route 192.168.1.96 255.255.255.224 172.16.1.2

ip route 192.168.1.128 255.255.255.224 172.16.1.2

ip route 192.168.1.160 255.255.255.224 172.16.1.2
```

🔁 Routeur Québec

ip route 192.168.1.32 255.255.255.224 172.16.2.2 # Montréal

ip route 192.168.1.64 255.255.255.224 172.16.2.2 # Gatineau

ip route 192.168.1.128 255.255.255.224 172.16.2.2 # Ottawa

ip route 192.168.1.160 255.255.255.224 172.16.2.2 # Direction Générale

- Add it to ths CLI of Québec Router with this:
```
ip route 192.168.1.32 255.255.255.224 172.16.2.2

ip route 192.168.1.64 255.255.255.224 172.16.2.2

ip route 192.168.1.128 255.255.255.224 172.16.2.2

ip route 192.168.1.160 255.255.255.224 172.16.2.2
```


🔁 Routeur Ottawa

ip route 192.168.1.32 255.255.255.224 172.16.4.2 # Montréal

ip route 192.168.1.64 255.255.255.224 172.16.4.2 # Gatineau

ip route 192.168.1.96 255.255.255.224 172.16.4.2 # Québec

ip route 192.168.1.160 255.255.255.224 172.16.4.2 # Direction Générale

- Add it to ths CLI of Ottawa Router with this:
```
ip route 192.168.1.32 255.255.255.224 172.16.4.2

ip route 192.168.1.64 255.255.255.224 172.16.4.2

ip route 192.168.1.96 255.255.255.224 172.16.4.2

ip route 192.168.1.160 255.255.255.224 172.16.4.2
```

🔁 Routeur Gatineau

ip route 192.168.1.32 255.255.255.224 172.16.3.2 # Montréal

ip route 192.168.1.96 255.255.255.224 172.16.3.2 # Québec

ip route 192.168.1.128 255.255.255.224 172.16.3.2 # Ottawa

ip route 192.168.1.160 255.255.255.224 172.16.3.2 # Direction Générale

- Add it to ths CLI of Gatineau Router with this:
```
ip route 192.168.1.32 255.255.255.224 172.16.3.2

ip route 192.168.1.96 255.255.255.224 172.16.3.2

ip route 192.168.1.128 255.255.255.224 172.16.3.2

ip route 192.168.1.160 255.255.255.224 172.16.3.2
```

🔁 Routeur Direction Générale

ip route 192.168.1.32 255.255.255.224 172.16.1.1 # Montréal

ip route 192.168.1.64 255.255.255.224 172.16.3.1 # Gatineau

ip route 192.168.1.96 255.255.255.224 172.16.2.1 # Québec

ip route 192.168.1.128 255.255.255.224 172.16.4.1 # Ottawa

- Add it to ths CLI of the Direction Generale Router with this:
```
ip route 192.168.1.32 255.255.255.224 172.16.1.1

ip route 192.168.1.64 255.255.255.224 172.16.3.1

ip route 192.168.1.96 255.255.255.224 172.16.2.1

ip route 192.168.1.128 255.255.255.224 172.16.4.1
```


## Here are the tests of validation:

- Ping PC's to PC's ping in different vlan's and the answers should be like this for every combination:

Here is a ping from PC7 to PC4 successful:

![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/ping%20PC7%20to%20PC4.png)

- Also I can use the PDU ![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/letter%20icon.png) and click with the envelloppe on the two devices I want to test communication. This should appear

![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/letter%20successful.png)

- Test the connection between PC12 and the web browser:
![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/web%20browsing%20pc12.png)

- Test the tracert of PC11 to the web server 192.168.1.163:
![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/tracert%20PC11%20web.png)


- FTP communication between PC15 and FTP server 192.168.1.164:

![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/ftp%20pc15.png)

- Do an nslookup for www.cumberland.college with PC13:
![image](https://github.com/RobinBoucherSec/Cisco-Packet-Tracer-Basic-Network/blob/main/pkt%20Static%20Routing/images/nslookup%20pc13.png)

## Problem encountered

- I realized that some PC where on static IP and not DHCP. I needed to enable the DHCP of the PC's in Desktop > IP Configuration.

- The configuration of Fa/192.168.1.165 of the Direction Generale's Router had a typo mistake so at first, vlan was not able to ping.

  ## 🔙 Back to Portfolio
[⬅️ Back to my Cybersecurity Portfolio](https://github.com/RobinBoucherSec/RobinBoucherSec)

