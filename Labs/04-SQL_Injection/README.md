# 04: SQL Injection

## SQL Injection

### Preparation

**Nessus does say it was unable to get version number for the MySQL server because it is restricted. Reflect on that.**

**Does it mean the MySQL server is protected against cyber attacks? From Kali, try:**  
`mysql -h <METASPLOITABLE IP> -P 3306`

No. Security by obscurity doesn't ensure that the MySQL server is protected against cyber attacks, however it makes it more difficult to find any vulnerabilities, but also hinders security researchers or ethical hackers to explore them with good intentions.

**How could that protection look like?**  


**And what exactly would it protect against?**  


### Spying with SQL Injection
**Please shortly discuss your opinion of this web server’s configuration concerning directly listings**

Relating to a PHP application server, we would argue for it's bad practice to let Apache 2 show the index of the root document folder. If this practice is done, the knowledge about hidden folders and files may be exposed, as well it could suggest to the attacker, that the server also might be misconfigured regarding file permissions.
