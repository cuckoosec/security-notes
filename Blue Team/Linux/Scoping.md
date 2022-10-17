## Network
```
#Ping-sweep
for ip in $(seq 254); do; ping -c1 -W1 192.168.42.$ip & done | grep from

#DHCP-leases
grep -Ei 'dhcpv4' /var/log/syslog

#DNS-logging
rndc querylog
```

## Hashing
```
#Hash all executables
find ./ -type f -exec md5sum {} >> md5sums.txt \;
```