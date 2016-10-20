[networks](index.md) |

## TCP/IP - Transmission Control Protocol/Internet Protocol

### - [Domain Name System (DNS)](DNS.md)

### - [Dynamic Host Configuration Protocol - DHCP](DHCP.md)

### - [HTTP](HTTP.md)

### - [hardware](hardware.md)


### I.P. Addresses
Divided up into 4 octets e.g.

`192.168.0.23`

each number between the dots is between 0 and 255 as that is the highest number that can be expressed by an octet

I.P. Addresses are typically 23 bits. Each octet is 8 bits & together they make up 32 bits (8 * 8 = 32).

The I.P. Address is separated into two sections, the network section & the host section. The network section is the 'address' of the network while the host section is the number of an individual computer. This is analogous to a street name & house number.

There are private & public I.P addresses. A router or residential gateway will have a public IP which is used on the internet, and a private IP which is only used within the home/office.

Localhost is typically 127.0.0.1


### Subnet Mask
The Subnet Mask is a dot-separated string of four octets, just like the I.P. Address. If we draw an imaginary line through the subnet mask between the last 255 from the left and the first zero, this shows us which part of the matching I.P. address is the network section & which is the host section.

e.g.

|`192.168.15.3` |
| ---- |
| `255.255.0.0` |

we can see that the first two octets of the IP, `192.168` are the network portion, & the `15.3` is the host portion

Subnet Mask | Binary | On's & Off's
---|---|---
255.0.0.0 | 11111111.00000000.00000000.00000000 | or 8 on & 24 off
255.255.0.0 | 11111111.11111111.00000000.00000000 | or 16 on & 16 off
255.255.255.0| 11111111.11111111.11111111.00000000 | or 24 on & 8 off


A subnet mask of `255.255.255.0` can be expressed as `192.168.15.3/24` because there are 24 switches on. This is called CIDR notation. The maximum number of bits which the network section of an IP address can be is 30 bits. You need at least 2 bits to represent the host section.

To find the available hosts, raise 2 to the power of however many bits are left to represent the hosts.. I.e. if there are 4 bits left then 2 to the power of 4. To find the usable hosts, subtract 2 from this number (for gateway & broadcast IP).

---

See also [binary notation](../math/binary.md)
