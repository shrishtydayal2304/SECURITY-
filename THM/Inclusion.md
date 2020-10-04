###### inclusion

##### we can start scanning using zenmap or namp
![image](https://user-images.githubusercontent.com/60177793/95021566-4bfe9e80-068f-11eb-89c3-7fe0ac9b0de5.png)
###### We see that port 22 ssh and port 80 is open and it is running a web server on opening the page using a web browser.
![image](https://user-images.githubusercontent.com/60177793/95021584-6cc6f400-068f-11eb-8cc3-f9248d6bcb3d.png)
##### I decided to do a gobuster on the webpage and got nothing so i decided to follow link view details and seeing the LFI, :
I decided to test for local file inclusion using that parameter. I decided to view a file that is common in all Linux operating system. Passwd
![image](https://user-images.githubusercontent.com/60177793/95021603-8d8f4980-068f-11eb-93dd-1b2bee8aefc3.png)
![image](https://user-images.githubusercontent.com/60177793/95021618-aef03580-068f-11eb-9a01-d10a29a581d6.png)
##### now we get a user shell as falconfeast. Now we can access the user flag as we kno  ssh was listening on port 22. 
![image](https://user-images.githubusercontent.com/60177793/95021642-d6df9900-068f-11eb-8333-d9ebf02b6f2d.png)
##### now for privilege escalation, we will do sudo -l; 
![image](https://user-images.githubusercontent.com/60177793/95021676-0c848200-0690-11eb-805d-e435ba2ec27a.png)
##### we get a way to exploit socat to get root privilege on GTFobins
![image](https://user-images.githubusercontent.com/60177793/95021923-8b2def00-0691-11eb-9da7-2dd9aa7096b7.png)
###### Decided to run the command on the target machine and created a listener in our local machine listening on port 4444 use: nc -lnvp 4444
##### Then executed the rest of the command on the target machine and the root shell will be executed
 






