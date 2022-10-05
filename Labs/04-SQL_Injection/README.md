# 04: SQL Injection

## SQL Injection

### Preparation

Nessus does say it was unable to get version number for the MySQL server because it is restricted. Reflect on that.

**Does it mean the MySQL server is protected against cyber attacks? From Kali, try:**  
`mysql -h <METASPLOITABLE IP> -P 3306`

No. Security by obscurity doesn't ensure that the MySQL server is protected against cyber attacks, however it makes it more difficult to find any vulnerabilities, but also hinders security researchers or ethical hackers to explore them with good intentions.

