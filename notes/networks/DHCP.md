[networks](index.md)

<!-- ## Dynamic Host Configuration Protocol -->
## Dynamic Host Configuration Protocol - DHCP

Takes care of assigning & unassigning I.P addresses to hosts. I.P. addresses by default are assigned dynamically by a DHCP server in exchange for the hosts MAC address, but can also be set manually. The server will have a pool of IP addresses available & these will be assigned when a host connects to that server.


1. Host sends out "Discover" message
2. DHCP server (router or specialised server) sends an "Offer" message with an IP address
3. Host sends a "request" message saying "Yes that looks good, can I use that one?"
4. DHCP server sends an "Ack" message (acknowledgement?)

---

See also ..
