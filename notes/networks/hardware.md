[networks](index.md) | [TCP/IP](TCP-IP.md)

## network hardware (backbones)

- [Hub](#hub)
- [Switch](#switch)
- [Router](#router)
- [MAC Address](mac-address)

### Hub
Layer 1 device, no addresses. It just repeats any data it receives. Except back to the sender. Half-duplex, means that it can't send & receive at the same time with out collisions, causing corruption of data & needing the hosts to send it again
- Wasted bandwidth
- Security risks
- Old tech, replaced by switches

### Bridge
Layer 2, can understand & learn MAC addresses. Segments LANs into smaller sections
- Fewer ports than a hub
- also replaced by switches.

### Switch
Layer 2 Device
Like a hub & a bridge joined together. Has a table of MAC addresses aka Layer 2 addresses. Full-duplex, can send & receive data at the same time. Multiple collision domains, each port can send & receive at the same time
- Saves bandwidth
- Increased Security
- Usually include a DHCP server

Modems?

### Router
Layer 3 Device
Doorway from your network to the outside world. In a home router, typically there would be a switch built in, although not in enterprise systems. Uses IP addresses (aka layer 3 addresses) & MAC addresses.
- Routes traffic between networks.
- Fewer ports.
- Highly configurable.

### MAC Address
Media Access Control address
A network adapters "ID", eg. 00-0F-1F-D4-65-E4
A media access control address (MAC address) of a computer is a unique identifier assigned to network interfaces for communications at the data link layer of a network segment. MAC addresses are used as a network address for most IEEE 802 network technologies, including Ethernet and WiFi. Logically, MAC addresses are used in the media access control protocol sublayer of the OSI reference model. (from [Wikipedia](https://en.wikipedia.org/wiki/MAC_address))


<!-- --- -->

<!-- See also -->
