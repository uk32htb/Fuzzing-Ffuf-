# Fuzzing-Ffuf

umarkhan$ ffuf -w /opt/useful/seclists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ -recursion -recursion-depth 1 -e .php -v :- This will search direstories and sub directories until the depth of 1 
umarkhan$ ffuf -w <SNIP> -u http://SERVER_IP:PORT/FUZZ :- This is for directory searching 
umarkhan$ ffuf -w /opt/useful/seclists/Discovery/Web-Content/directory-list-2.3-small.txt:FUZZ -u http://SERVER_IP:PORT/blog/FUZZ.php :- Fuzzing all the files with extension PHP 

Commands to enumerate sub-domains 
umarkhan$ ffuf -s -w /opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt:FUZZ -u http://FUZZ.inlanefreight.com


Commands to get VHOST 
umarkhan:$ ffuf -s -w /opt/useful/SecLists/Discovery/DNS/subdomains-top1million-5000.txt:FUZZ -u http://academy.htb:31145/ -H 'Host: FUZZ.academy.htb' -ac :- ALWAYS use this mate!! 
