Ansible role to configure an IPSec VPN with virtual tunnel interface

See [this blog post](https://cybercyber.org/site-to-site-vpn-using-ipsec-virtual-tunnels-and-bgp.html) for an extended use-case.

Supply the variable `ipsec_peers` with this content:

```yaml
ipsec_peers:
- name: ... # the name of the connection
  psk: ... # the PSK of the connection
  ipsec_net: ... # the network (CIDR) of the virtual interface (e.g. 192.168.44.5/30)
  other: ... # the ip address of the other host
  routes: ... # a list of CIDRs that should routed over the virtual tunnel interface
  me: ... # The local ip to use
  myid: ... # The id to use
```
