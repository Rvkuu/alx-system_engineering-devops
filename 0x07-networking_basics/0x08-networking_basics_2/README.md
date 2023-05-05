In computer networking, localhost is a hostname that refers to the current computer used to access it. It is used to access the network services that are running on the host via the loopback network interface. Using the loopback interface bypasses any local network interface hardware.

Loopback
The local loopback mechanism may be used to run a network service on a host without requiring a physical network interface, or without making the service accessible from the networks the computer may be connected to. For example, a locally installed website may be accessed from a Web browser by the URL http://localhost to display its home page.

The name localhost normally resolves to the IPv4 loopback address 127.0.0.1, and to the IPv6 loopback address ::1.[1]

Name resolution
IPv4 network standards reserve the entire address block 127.0.0.0/8 (more than 16 million addresses) for loopback purposes.[2] That means any packet sent to any of those addresses is looped back. The address 127.0.0.1 is the standard address for IPv4 loopback traffic; the rest are not supported by all operating systems. However, they can be used to set up multiple server applications on the host, all listening on the same port number. The IPv6 standard assigns only a single address for loopback: ::1.

The resolution of the name localhost to one or more IP addresses is normally configured by the following lines in the operating system's hosts file:

127.0.0.1    localhost
::1          localhost
The name may also be resolved by Domain Name System (DNS) servers, but queries for this name should be resolved locally, and should not be forwarded to remote name servers.

In addition to the mapping of localhost to the loopback addresses (127.0.0.1 and ::1), localhost may also be mapped to other IPv4 (loopback) addresses and it is also possible to assign other, or additional, names to any loopback address. The mapping of localhost to addresses other than the designated loopback address range in the hosts file or in DNS is not guaranteed to have the desired effect, as applications may map the name internally.

In the Domain Name System, the name localhost is reserved as a top-level domain name, originally set aside to avoid confusion with the hostname used for loopback purposes.[3] IETF standards prohibit domain name registrars from assigning the name localhost.
The Internet Protocol Version 4 address 0.0.0.0 can have multiple uses.

Official Standard Meaning and Use
IANA, who allocate IP addresses globally, have allocated the single IP address 0.0.0.0[1] to RFC 1122 section 3.2.1.3.

It is named there as "This host on this network"

RFC 1122 refers to 0.0.0.0 using the notation {0,0}. It prohibits this as a destination address in IPv4 and only allows it as a source address under specific circumstances.

A host may use 0.0.0.0 as its own source address in IP when it has not yet been assigned an address. Such as when sending the initial DHCPDISCOVER packet when using DHCP.

Internal Operating system Specific Uses
Some operating systems have attributed special internal meaning to the address. These uses do not result in IPv4 packets containing 0.0.0.0 and so are not necessarily governed by RFC 1122.[2] These meanings may not be consistent between OS.

In both Windows and Linux, when selecting which of a host's IP address to use as a source IP, a program may specify INADDR_ANY (0.0.0.0). [3][4]

In Linux a program may specify 0.0.0.0 as the remote address to connect to the current host (AKA localhost).

Other non-standard Uses
Besides the use by operating systems internally, other uses have been attributed to the address with varying success[5][6]

A non-routable meta-address used to designate an invalid, unknown or non applicable target
The address a host assigns to itself when address request via DHCP has failed, provided the host's IP stack supports this. This usage has been replaced with the APIPA mechanism in modern operating systems.
A way to explicitly specify that the target is unavailable.[7]
A way to route a request to a nonexistent target instead of the original target. Often used for adblocking purposes. This can conflict with OS specific behaviour. For example use in DNS can cause Linux to connect to Localhost instead of nothing at all.[8]
Routing
In routing tables, 0.0.0.0 can also appear in the gateway column. This indicates that the gateway to reach the corresponding destination subnet is unspecified. This generally means that no intermediate routing hops are necessary because the system is directly connected to the destination.[9]

This should not be confused with the CIDR notation 0.0.0.0/0 which defines an IP block containing all possible IP addresses. It is commonly used in routing to depict the default route as a destination subnet. It matches all addresses in the IPv4 address space and is present on most hosts, directed towards a local router.

In IPv6
In IPv6, the all-zeros address is typically represented by :: (two colons), which is the short notation of 0000:0000:0000:0000:0000:0000:0000:0000.[10] The IPv6 variant serves the same purpose as its IPv4 counterpart.
