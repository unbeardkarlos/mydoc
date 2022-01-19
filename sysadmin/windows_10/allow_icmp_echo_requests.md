# Allow ICMP echo request on windows 10

in first time open command prompt as administrator.

then execute this command to allow ICMP echo request for IPV4
```
netsh advfirewall firewall add rule name="ICMP Allow incoming V4 echo request" protocol=icmpv4:8,any dir=in action=allow
```

and this if you want to allow ICMP echo request for IPV6
```
netsh advfirewall firewall add rule name="ICMP Allow incoming V6 echo request" protocol=icmpv6:8,any dir=in action=allow
```

now you can ping from remote host. 

tested and working on windows 10, 7 ...
