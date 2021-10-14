Ansible role to configure an IPSec VPN with virtual tunnel interface

Supply the variable `ipsec_peers` with this content:

```yaml
ipsec_peers:
- name: ... # the name of the connection
  psk: ... # the PSK of the connection
  ipsec_net: ... # the network (CIDR) of the virtual interface (e.g. 192.168.44.5/30)
  other: ... # the ip address of the other host
  routes: ... # a list of CIDRs that should routed over the virtual tunnel interface
```
