%title: Streisand Workshop - become your own VPN provider
%author: @hydrandt|lukas@aiya.cz
%date: 2016-04-09

-> # Streisand - a set of Ansible roles that sets up a multi-protocol VPN server

-> *https://github.com/jlund/streisand*

* presentation created using [mdp](https://github.com/visit1985/mdp)


## Workshop 
1. what is Streisand
2. what is Ansible
3. good servers locations and providers
5. everybody gets a server!
6. deploying Streisand
7. what has been deployed?
8. VPN protocols
9. tweak it: add accounts, shadowsocks tricks,...

---

# $ whoami
lukas

* free software and culture enthusiast
* Chinese studies graduate
* interested in censorship, media control, freedom, security
* sysadmin


## My workflow:

-> ▛▀▀▀▀▀▀▀▀▀▀▀▀▀▜          ▛▀▀▀▀▀▀▀▀▀▀▀▀▀▀▜
-> ▌broken server▐  ----->  ▌working server▐
-> ▙▄▄▄▄▄▄▄▄▄▄▄▄▄▟          ▙▄▄▄▄▄▄▄▄▄▄▄▄▄▄▟


---

# $ whoareyou

-> Introduce yourself, please!

---

# What is Streisand

-> *https://github.com/jlund/streisand*
-> by *Joshua Lund* @joshualund, "Sysadmin, programmer, privacy activist, security enthusiast, writer, and occasional cyclist."

## Set of Ansible roles that configures a VPN gateway accessible via:

* shadowsocks
* l2tp/ipsec (libreswan and xl2tpd)
* openconnect / cisco anyconnect
* openvpn (udp, tcp, through stunnel)
* ssh
* tor with obfsproxy

on any Ubuntu 14.04 server

---

# What is Streisand

* can automatically spin-up a VPS on Amazon EC2, DigitalOcean, Google Compute Engine, Linode, and Rackspace
* password-protected website with custom-generated instructions how to connect
* monit to automatically restart unresponsive services
* tinyproxy, if your application doesn't suport socks
* dnsmasq for your DNS queries
* sslh to have everything available on port 443 at the same time (for restricted networks)
* unattended-upgrades, so it stays up-to-date with security patches
* no logging

---

# What is Ansible

* orchestration tool
* agent-less (remote side must have ssh and python)
* playbooks = recipes how to cook a server = description of a system. In yaml.
* idempotent

---

# Where to get a server

* Digital Ocean
* Linode
* Chunkhost
* Amazon EC2
* Rackspace
* ...your recommendation?

---

# Digital Ocean

* digitalocean.com; my referral link: https://m.do.co/c/8523367ec739
* quite a few promos - use FLOSS to get $10 and support [FLOSS weekly](https://twit.tv/shows/floss-weekly), great podcast about free and libre open source software

*  $5/month: 1 core, 512MB RAM, 20GB SSD, 1TB transfer
* $10/month: 1 core,   1GB RAM, 30GB SSD, 2TB transfer
* $20/month: 2 core,   2GB RAM, 40GB SSD, 3TB transfer
* San Francisco, Singapore, London, Frankfurt, Amsterdam, New York, Toronto
* 1Gbps up/down interface 

* San Francisco: ~180 ms, good speeds
* Singapore: via US, ~250 ms, not good
* London: ~200 ms
* Frankfurt: ~220 ms

---

# Linode

* linode.com; my referral link: https://www.linode.com/?r=4963024da4675f3c6fe4503c055803472468ed40
* $10/month: 1 core, 1GB RAM, 24GB SSD, 2TB transfer, 40Gbps in, 125Mbps out
* $20/month: 2 core, 2GB RAM, 48GB SSD, 3TB transfer, 40Gbps in, 250Mbps out
* Singapore (good), Tokyo (good, sold out), US East/Central/West, London, Frankfurt

---

# Chunkhost

* chunkhost.com; my referral link: https://chunkhost.com/r/45017
* LA only; good peering with Chinese telcos; ~150ms; I use it all the time
* Yearly payment: $5/month: 1GB of RAM, 20GB SSD, 4TB transfer
* Accepts bitcoin! (don't have a credit card? :-)

---

# -> Let's get a server, everyone!

---

# Login to our ssh gateway

ssh (/mosh) workshop$i@la.aiya.cz; password streisand.workshop$i.pw

# create ssh key: ssh-keygen


---

# Deploy Streisand!

-> All instructions on https://github.com/jlund/streisand#prerequisites

---

-> Take your freedom in your hands.

-> Spread the word!

-> Thank you!

