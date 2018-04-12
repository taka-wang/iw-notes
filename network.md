# Network Concepts

## General

- [Linux Networking Explained, 2016, Toronto](https://goo.gl/irrnwa)
- ip 與 ifconfig 指令比較 -> [ifconfig vs ip](https://p5r.uk/blog/2010/ifconfig-ip-comparison.html)
- 一些簡易的netns操作 -> [Introducing Linux Network Namespaces](https://blog.scottlowe.org/2013/09/04/introducing-linux-network-namespaces/)

## Terminology

- Network interfaces
- L2, L3
  - [Layer 2 versus Layer 3 services: A Dummies Guide](http://www.vertel.com.au/blog/layer-2-versus-layer-3-services-a-dummies-guide)
- IP forwarding
  - IP forwarding should be enabled when you want the system to **act as a router**, that is transfer IP packets from one network to another.
  - IP forwarding involves transferring packets **between network interfaces**.
  - Ref: [IP Forwarding = when and why is this required?](https://serverfault.com/questions/248841/ip-forwarding-when-and-why-is-this-required)
- ARP
  - [Taking a fresh look at the address resolution protocol](http://techgenix.com/address-resolution-protocol/)
  - [Understanding Man-in-the-Middle Attacks - ARP Cache Poisoning (Part 1)](http://techgenix.com/understanding-man-in-the-middle-attacks-arp-part1/)
- Default Gateway
- Bridge
- DNS
- Proxy
- Veth (Virtual **ethernet** interface)
  - A veth device has a MAC address
  - **veth pair** 是用於不同 network namespace 間進行通信的方式，veth pair 將一個 network namespace 數據發往另一個 network namespace 的 veth
  - Virtual Ethernet interfaces come in pairs, and they are connected like a tube—whatever comes in one veth interface will come out the other peer veth interface. As a result, you can use veth interfaces to connect a network namespace to the outside world via the “default” or “global” namespace where physical interfaces exist. [REF](https://stackoverflow.com/questions/25641630/virtual-networking-devices-in-linux)
  - They can act as tunnels between network namespaces to create a bridge to a physical network device in another namespace, but can also be used as standalone network devices.
  - Packets transmitted on one device in the pair are immediately received on the other device.  
  - When either devices is down the link state of the pair is down.
  - Hands-on -> [Introducing Linux Network Namespaces](https://blog.scottlowe.org/2013/09/04/introducing-linux-network-namespaces/)

- Network Namespaces
  - [Linux: Network Namespace](http://abregman.com/2016/09/29/linux-network-namespace/)
  - [Introducing Linux Network Namespaces](https://blog.scottlowe.org/2013/09/04/introducing-linux-network-namespaces/)
  - [Unweaving the web - Network namespaces](https://blogs.igalia.com/dpino/2016/04/10/network-namespaces/)
  - [Namespaces in operation, part 7: Network namespaces](https://lwn.net/Articles/580893/)

- Overlay networks
  - [A container networking overview](https://jvns.ca/blog/2016/12/22/container-networking/) :thumbsup:
  - [Demystifying Docker overlay networking](http://blog.nigelpoulton.com/demystifying-docker-overlay-networking/)

- Route tables
  - How to run `ip route list` and `ip link list`
  - Basics about how to use iptables & read iptables configuration
  - [Linux Advanced Routing Tutorial](https://www.linuxjournal.com/content/linux-advanced-routing-tutorial)
  - 自訂 policy Routing操作 -> [A Quick Introduction to Linux Policy Routing](https://blog.scottlowe.org/2013/05/29/a-quick-introduction-to-linux-policy-routing/)

- Encapsulation (vxlan(Virtual Extensible LAN) / UDP)

- TLS, server certs, `client certs` (X509), certificate authorities
  - [How Kubernetes certificate authorities work](https://jvns.ca/blog/2017/08/05/how-kubernetes-certificates-work/)

- CIDR Notation
  - [Understanding IP Addresses, Subnets, and CIDR Notation for Networking](https://www.digitalocean.com/community/tutorials/understanding-ip-addresses-subnets-and-cidr-notation-for-networking)
  - [twbsd - ch05 網路設定](https://www.twbsd.org/cht/book/ch05.htm)
---

