## Net Discovery
```
net view /all
net view \\<HOST>

# Ping scan and output
for \L %I in (1,1,254) do ping -w 30 -n 1 10.1.1.%I | find "Reply" >> <OUTFILE>.txt
```

## DNS
```
#Enable logging
DNSCmd <SERVER> /config /logLevel 0x8100F331

#Log location
DNSCmd <SERVER> /config /LogFilePath <C:\Path\To\Log\File>

# Set log size
DNSCmd <SERVER> /config /logfilemaxsize 0xffffffff
```

## Hashing
```
PS C:\> Get-FileHash -algorithm md5 <FILE>
certutil -hashfile <FILE> SHA1
```

## AD Inventory
```
# List all OUs
dsquery ou DC=<DOMAIN>,DC=<DOMAIN EXTENSION>

# Workstations in domain
netdom query WORKSTATION
netdom query SERVER
netdom query OU

# List DCs
netdom query DC
netdom query PDC #primary
netdom query TRUST

#List all computers from AD
dnsquery COMPUTER "OU=servers,DC=<DOMAIN NAME>,DC=<DOMAIN EXTENSION>" -o rdn -limit 0 > C:\machines.txt

#Accounts inactive longer than 3 weeks
dnsquery user domainroot -inactive 3

#Dump new AD accounts in last 90 Days (PowerShell)
import-module activedirectory
Get-QADUser -CreatedAfter (Get-Date).AddDays(-90)
Get-ADUser -Filter * -Properties whenCreated | Where-Object {$_.whenCreated -ge ((Get-Date).AddDays(-90)).Date}

```