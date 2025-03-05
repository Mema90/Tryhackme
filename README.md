# Tryhackme
Q1: How many services are running under port 1000?
Sol: nmap -sV -sC ip -p1-1000

Q2: What is running on the higher port?
Sol: nmap ip , its need name of port not number 
Q3: What’s the CVE you’re using against the application?
to find that we need to make gobuster bez when put nmuber of port next to ip nothing appear so 
gobuster dir -u http:ip:number_of_port -w /usr/share/wordlists/dirbuster/directory-list-
2.3-medium.txt -t 100
we get simple.txt 
now put in in link 
http:ip/simple.txt 
to get name of devlop web 
CMS made simple 2.2.8
search in google to get cve 
Sol:CVE-2019–9053
Q4: To what kind of vulnerability is the application vulnerable?
the website for cve its mean sql 
Sol: sqli 
