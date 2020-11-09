
![image](https://user-images.githubusercontent.com/60177793/98545056-e4a1c300-22ba-11eb-8c3c-fbf6cf8f01da.png)
## Scanning
#### using zen-map or nmap we can scan:
## How many ports are open?
### ans 2
![image](https://user-images.githubusercontent.com/60177793/98545116-000cce00-22bb-11eb-9c2e-016cabd3bc3b.png)
##  What version of SSH is running?
### ans  OpenSSH 7.6p1
![image](https://user-images.githubusercontent.com/60177793/98545343-5b3ec080-22bb-11eb-94f4-2f3580c4ac53.png)
## What version of Apache is running?
### ans  2.4.29
![image](https://user-images.githubusercontent.com/60177793/98545382-698cdc80-22bb-11eb-8044-f0e950e1714d.png)
## Which Linux distribution is running?
ans ubuntu
## Search for hidden directories on web server.What is the hidden directory?
### for this..we will use gobuster:
![image](https://user-images.githubusercontent.com/60177793/98545504-99d47b00-22bb-11eb-97f3-a8a1b75ac272.png)

### ans /admin
![image](https://user-images.githubusercontent.com/60177793/98545547-a78a0080-22bb-11eb-938e-5330d19f0a8e.png)
### checking the page source , i found a hidden msg which gives the username ;admin
![image](https://user-images.githubusercontent.com/60177793/98545665-d2745480-22bb-11eb-9ba0-26e5dc21f12c.png)
### now for password we can use hydra
![image](https://user-images.githubusercontent.com/60177793/98545734-ea4bd880-22bb-11eb-8fa1-e0333b655fe7.png)

## What is the user:password of the admin panel?
### ans admin:xavier 
### rsa private key
![image](https://user-images.githubusercontent.com/60177793/98545824-0fd8e200-22bc-11eb-9707-a224dc1c86c7.png)
### Web flag
### ans THM{brut3_f0rce_is_e4sy}
![image](https://user-images.githubusercontent.com/60177793/98545842-15cec300-22bc-11eb-8125-c748d68a6386.png)
![image](https://user-images.githubusercontent.com/60177793/98545843-15cec300-22bc-11eb-954c-3e5d6a2f81ed.png)
### try to ssh login
![image](https://user-images.githubusercontent.com/60177793/98545909-30a13780-22bc-11eb-8b1f-df3bfc875b8d.png)
 ### we need to find the passphrase too!!!

![image](https://user-images.githubusercontent.com/60177793/98546114-778f2d00-22bc-11eb-94ee-57ad32df4094.png)

![image](https://user-images.githubusercontent.com/60177793/98546149-81b12b80-22bc-11eb-93a8-6f9c08ae2b57.png)
### Crack the RSA key you found.
## What is John's RSA Private Key passphrase?
### rockinroll



