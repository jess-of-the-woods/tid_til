[networks](index.md) | []()

## TCP / IP - Transmission Control Protocol / Internet Protocol


**[HTTP](HTTP.md)**

### I.P. Addresses
Divided up into 4 octets e.g.

`192.168.0.23`

each number between the dots is between 0 and 255 as that is the highest number that can be expressed by an octet


The I.P. Address is separated into two sections, the network section & the host section.

### Subnet Mask
The Subnet Mask is a dot-separated string of four octets, just like the I.P. Address. If we draw am imaginary line through the subnet mask between the last 255 from the left and the first zero, this shows us which part of the matching I.P. address is the network section & which is the host section.

e.g.

| `192.168.56.99` |
| -- | -- |
| `255.255.0.0` |

we can see that the first two octets of the IP, `192.168` are the network, & the `56.99` is the host

---

See also [math](../math.md)
