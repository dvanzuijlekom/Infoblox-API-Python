# Infoblox API

This project implements the subset of Infoblox API via REST API

## Infoblox API python module

Class **Infoblox** implements the following methods:

- create_network
- delete_network
- create_networkcontainer
- delete_networkcontainer
- create_host_record
- delete_host_record
- add_host_alias
- delete_host_alias
- create_cname_record
- delete_cname_record
- create_dhcp_range
- delete_dhcp_range
- get_next_available_ip
- get_host
- get_host_by_ip
- get_ip_by_host
- get_host_by_extattrs
- get_host_extattrs
- get_network
- get_network_by_ip
- get_network_by_extattrs
- get_network_extattrs
- update_network_extattrs
- delete_network_extattrs

* * *

### How to use

Example:

```
import infoblox

iba_api = infoblox.Infoblox('10.10.20.32', 'admin', 'secret', '1.0', 'internal', 'default')

try:
    ip = iba_api.get_next_available_ip('192.168.0.0/24')
    iba_api.create_host_record(ip, 'mytest.example.com')
except Exception as e:
    print e

```

### Limitations

Currently supports WAPI 1.0 only. 1.2.1 is coming soon.
