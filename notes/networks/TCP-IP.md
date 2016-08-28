[networks](index.md) | []()

## TCP / IP - Transmission Control Protocol / Internet Protocol


**[HTTP](HTTP.md)**

### I.P. Addresses
Divided up into 4 octets e.g.

`192.168.0.23`

each number between the dots is between 0 and 255 as that is the highest number that can be expressed by an octet


The I.P. Address is separated into two sections, the network section & the host section. The network section is the 'address' of the network while the host section is the number of an individual computer. This is analogous to a street name & house number.

### Subnet Mask
The Subnet Mask is a dot-separated string of four octets, just like the I.P. Address. If we draw am imaginary line through the subnet mask between the last 255 from the left and the first zero, this shows us which part of the matching I.P. address is the network section & which is the host section.

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


A subnet mask of `255.255.255.0` can be expressed as `192.168.15.3/24` because there are 24 switches on.

---

See also [math](../math.md)
