# Agent sudo

![image](https://user-images.githubusercontent.com/60177793/93885073-5ae56880-fd01-11ea-989d-6d8ab142ea34.png)

![image](https://user-images.githubusercontent.com/60177793/93885313-a1d35e00-fd01-11ea-9591-51ca7b7e19e0.png)
![image](https://user-images.githubusercontent.com/60177793/93885462-c8919480-fd01-11ea-87af-20c845ad6369.png)
![image](https://user-images.githubusercontent.com/60177793/93885598-f2e35200-fd01-11ea-9845-46d6a35d7768.png)
![image](https://user-images.githubusercontent.com/60177793/93885667-0c849980-fd02-11ea-81f1-74f8085dc1db.png)
![image](https://user-images.githubusercontent.com/60177793/93885699-16a69800-fd02-11ea-81ac-193b89afbc4e.png)



###### Tried to use gobuster to get some usefull info..but it showed no usefull info
![image](https://user-images.githubusercontent.com/60177793/93984741-d39c0180-fda1-11ea-822c-6f5aca08150d.png)
###### ftp login on server using the username an pass:- chris : crystal
![image](https://user-images.githubusercontent.com/60177793/93984859-f7f7de00-fda1-11ea-9ac5-3f260fc7bf91.png)
![image](https://user-images.githubusercontent.com/60177793/93984889-0219dc80-fda2-11ea-9721-32ddbf288cd6.png)
###### checking the content of those image and txt file 
![image](https://user-images.githubusercontent.com/60177793/93984950-1362e900-fda2-11ea-8d76-52c5cc2c1e13.png)
![image](https://user-images.githubusercontent.com/60177793/93984998-1cec5100-fda2-11ea-8de8-0c1de75c2800.png)
![image](https://user-images.githubusercontent.com/60177793/93985028-24abf580-fda2-11ea-963a-27bf8a8819ed.png)
###### So we used “zip2john” to crack the zip file for password with this command
###### ./zip2john 8702.zip > Output.txt and then we used john to crack the hash.

![image](https://user-images.githubusercontent.com/60177793/93985264-72286280-fda2-11ea-9f28-b34faaafae92.png)
![image](https://user-images.githubusercontent.com/60177793/93985300-7ce2f780-fda2-11ea-849c-a0dd03ec1f39.png)

###### This message was from Agent R we decoded this ‘Q*******’ message using echo base | base64 -d
![image](https://user-images.githubusercontent.com/60177793/93985418-aef45980-fda2-11ea-9444-f44e37c939f0.png)
###### Now we logged in through SSH into the machine using the username and password we found now we can read the user flag

![image](https://user-images.githubusercontent.com/60177793/93985501-cdf2eb80-fda2-11ea-991f-35d8b15986b1.png)

![image](https://user-images.githubusercontent.com/60177793/93985712-10b4c380-fda3-11ea-9302-2df6dba2cdc9.png)
![image](https://user-images.githubusercontent.com/60177793/93986138-933d8300-fda3-11ea-960c-e19ebc6de6b2.png)


# Privilege Esclation
###### We checked for the permission the user has with “sudo -l” command.
![image](https://user-images.githubusercontent.com/60177793/93985817-317d1900-fda3-11ea-858c-c51c96046d24.png)
###### We searched on google and we got a vulnerability for Sudo for version 1.8.28 so we checked the version of sudo
###### Our sudo version is lower from 1.8.28 so we can exploit the machine.
![image](https://user-images.githubusercontent.com/60177793/93985889-4659ac80-fda3-11ea-9cfa-ac8a9779581a.png)

###### Well, we are root now!





