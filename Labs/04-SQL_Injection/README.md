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

**What type of SQLi attack works? Can you explain why?**  
* Boolean-based
* Union-based

Boolean-based SQL injection attacks work in this context, as we are able to access all rows by determining a WHERE clause that is always true.

Union-based attacks work too, an example of how is shown below.


**What service is running there?**
```
$ nmap -sV -p 3306 13.37.0.6

Starting Nmap 7.92 ( https://nmap.org ) at 2022-10-05 11:25 EDT
Nmap scan report for ms (13.37.0.6)
Host is up (0.00077s latency).

PORT     STATE SERVICE VERSION
3306/tcp open  mysql   MySQL (unauthorized)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 0.30 seconds
zsh: segmentation fault  nmap -sV -p 3306 13.37.0.6
```

According to the nmap search, it's MySQL Server.

**What is the \# sign for?**
It's a comment, preventing additional queries to execute, that could affect the displayed result - especially using UNION SQL injection attacks.

**What do you notice about these passwords? What would you change to secure them?**  
The passwords are stored (virtually at least) in plain text, therefore a database leak could result in these informations being published, which could lead to unauthorized access to both this service and external services (studies find that most Danes use the same password twice).

An improvement would be to use PBKDF2, Argon2 or Bcrypt, which are hashing mechanics, that also uses random bit generators to mitigate the risk of reverse-databases, that for instance are available to SHA and MD5.


