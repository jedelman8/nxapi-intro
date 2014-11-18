HOW TO
===========

Python modules to simplify the use of NX-API

```python
switch = Device(ip='192.168.200.50')
switch.open()

show_command = switch.show('show version')

# optionally convert to a dictionary
show_version = xmltodict.parse(show_command[1])

# push a config

push_config = switch.conf('config t ; interface eth1/1 ; no shut')

# credentials are stored in device.py - can change there or use:
switch = Device(ip='192.168.200.50',username='cisco',password='cisco')
```


