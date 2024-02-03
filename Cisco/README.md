### Nützliche Show Befehle zum Troubleshooting
Zeigt eine Zusammenfassung ob Interfaces Up oder down, differenziert über 2 Ebenen. Einmal Layer 1 Up / Down und Layer 2 Up/Down
show ip interface brief

Zusammenfassung der angelegten VLAN´s und wem welchem VLAN welcher Port zugewiesen ist
show vlan

Zeigt an welche direkten Nachbarswitche angeschlossen sind
show cdp neighbors

Niemals das speichern vergessen
write memory
oder wenn im Config Mode
do write memory


### Neues VLAN anlegen
vtp mode transparent
vlan %16%
name %Gast-EPH%
interface vlan %16%
description %Gast-EPH%
no shutdown

### Switchport bestimmtes VLAN zuweisen
interface %GI0/1%
switchport mode access
switchport access vlan %16%
spanning-tree portfast
spanning-tree bpduguard enable

### Switchport als Trunk definieren
switchport mode trunk
description %"Trunk nach xyz"%
switchporttrunk encapulation dot1q
description %"Trunk nach xyz"%

### SNMPv3 einrichten
snmp-server group SNMPV3 v3 priv write v1default
snmp-server group SNMPV3 v3 auth context vlan- match prefix (or snmp-server group SNMPV3 v3 auth context vlan-253 read v1default) 
snmp-server user snmpv3user SNMPV3 v3 auth sha password priv aes 128
password
snmp-server host 172.31.248.50 version 3 priv snmpv3user

### Network Access Control
interface FastEthernet0/1
switchport mode access

### Stack Member 2 Boot Image zuweisen
einfügen
