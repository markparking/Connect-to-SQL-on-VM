
This guide assumes you already have an SQL server and SQL management studio installed, an SQL user, has SQL authentication enabled, and correct IP configuration.


## Steps

##### Server Configuration Manager
1. Open SQL Server Configuration Manager
2. Click SQL Server Network Configuration in the left panel
3. Click protocols for "Servername"
4. Right click TCP/IP - click "Enable"
5. Right click TCP/IP again, now clicking properties
6. Select the IP Adresses tab, and make sure your TCP Ports are all 1433 and IP2 IP Adress is correct.
7. Click apply.

#### Firewall rule
1. Open Windows Defender Firewall with Advanced Security
2. Right click "Inbound Rules"
3. Select New Rule
4. Selecty Port, and click next.
5. Check TCP, and "Specific local ports" - write 1433 in the field.
6. Click next, and select "Allow the connection"
7. Click next, and select Private, Domain, and public.
8. Click apply.


#### Testing connection to sql

1. Open SQL Management Studio on the Host PC.
2. In servername, fill out the IP-adress of the VM, followed by a comma, the port, and \SQLEXPRESS - Example: **192.168.1.20,1433\\SQLEXPRESS**
3. Select "SQL Authentication"
4. Fill out the created username, and password.

