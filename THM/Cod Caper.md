# The Cod Caper room

# Host Enumeration
##### So first we started with a Nmap scan to see open ports and services are running on the machine.
![image](https://user-images.githubusercontent.com/60177793/95357319-56b27100-08e5-11eb-9f9a-1ce98e7dc330.png)
##### There are two open ports on the target machine and we can see the “ssh” service version, web server version.
#Web Enumeration
##### Port 80 was open so we checked in the browser.
![image](https://user-images.githubusercontent.com/60177793/95357443-7c3f7a80-08e5-11eb-8c8b-196f0d9d2440.png)
##### The default webpage of Apache is there so we can try to get directoriesusing bruteforce technique  from the “gobuster” tool.
![image](https://user-images.githubusercontent.com/60177793/95357697-d50f1300-08e5-11eb-99b8-108a7cb99cc5.png)
# Web Exploitation
![image](https://user-images.githubusercontent.com/60177793/95357802-f243e180-08e5-11eb-9790-cd214aea2fc7.png)
##### We got the Admin login page but we don’t have credentials to log in so we tried to do SQL injection using the “sqlmap” tool.
Flags we used
“ -u” to specify the URL.
“ — forms” to Automatic select the parameters.
“ — dump” to get data once SQLI is found.
![image](https://user-images.githubusercontent.com/60177793/95357952-228b8000-08e6-11eb-840a-3346ef812680.png)
![image](https://user-images.githubusercontent.com/60177793/95357986-2b7c5180-08e6-11eb-8cc1-e2f75d713b64.png)
##### After login, we have a command prompt it seems we have got the ability to run commands. like i tried ls , so we will try id and whoami to know more info and use netcat 




##### SSH 
![image](https://user-images.githubusercontent.com/60177793/95489948-23d7ae00-09b5-11eb-9e00-e4d1ce71c2a3.png)




