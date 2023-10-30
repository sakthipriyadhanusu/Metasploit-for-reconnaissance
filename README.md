# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## PROGRAM:
Find out the ip address of the attackers system

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/b442ed4f-4821-4c24-a2e8-d5f2d37d34d7)

## invoke msfconsole:
## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/e796ff01-a57c-47e7-ae04-d525ed2656e7)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/fb38679c-b193-4e0f-a375-09406b60f6a5)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/59ebf1d4-d396-43cf-9cab-02e77fbd9f41)
scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/6e3a36ba-b0c1-4ff7-a66b-bae6a511f2a9)
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/21c89a5c-388d-4cfa-a884-88be5a21d9ed)
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/1847e488-966b-4d1d-b7cc-dc3ad20c2a23)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/1c433cc1-0965-41ba-95bf-f13c762f4d6a)
The info command provides information regarding a module or platform

## OUTPUT:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/c90cf535-307b-4747-b2c3-c9d918eda9fe)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/0f97c7a4-5077-4006-b17c-c0e36ed91619)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/c5ad85da-90e2-41e4-950e-bc4faecf6326)
use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/78ad0246-be3b-4303-9f6d-820c631fba83)
Use the set rhosts command to set the parameter and run the module, as follows:
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/06be97df-d631-4058-92c6-03d7358e968b)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/fa772d0c-8c60-4a7d-8921-10f6e983d87a)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true
![image](https://github.com/sakthipriyadhanusu/Metasploit-for-reconnaissance/assets/119393194/ee627083-15fb-418b-abcf-d821985e02da)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
