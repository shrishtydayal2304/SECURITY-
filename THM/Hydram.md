# Hydra walkthrough
![image](https://user-images.githubusercontent.com/60177793/91703187-6d9fce00-eb97-11ea-80d0-4df5170dccc0.png)
# Task-1 Hydra Introduction
![image](https://user-images.githubusercontent.com/60177793/91703545-fb7bb900-eb97-11ea-8915-39efb8a148a8.png)
# Task-2 Using Hydra

![image](https://user-images.githubusercontent.com/60177793/91704859-c40e0c00-eb99-11ea-9f7d-9c874f7a20a8.png)

![image](https://user-images.githubusercontent.com/60177793/91703909-8f4d8500-eb98-11ea-8bae-226d38ba7b0d.png)
![image](https://user-images.githubusercontent.com/60177793/91704124-c91e8b80-eb98-11ea-82a6-8d98b3059b02.png)
![image](https://user-images.githubusercontent.com/60177793/91704280-084cdc80-eb99-11ea-9872-fc10eace814d.png)
# Now will submit the username:molly and password:sunshine on the login page and we will get the flag as shown below:
![image](https://user-images.githubusercontent.com/60177793/91704314-14389e80-eb99-11ea-9dc7-d6b445269e2e.png)

# 2 )Use Hydra to bruteforce molly’s SSH password. What is flag 2?
# Answer : THM{c8eeb0468febbadea859baeb33b2541b}
###### Steps: This can be done using command (hydra -l molly -P rockyou.txt ssh -V). You will get password and then login to ssh using this command (ssh molly@IP). Now ‘ls’ and ‘cat’ the flag.
![image](https://user-images.githubusercontent.com/60177793/91706358-eacd4200-eb9b-11ea-85dd-11c3fb518693.png)
###### Use the hydra command for ssh
![image](https://user-images.githubusercontent.com/60177793/91706384-f456aa00-eb9b-11ea-9b2a-4e9f1bc32e01.png)
###### Now login using ssh username@ip
![image](https://user-images.githubusercontent.com/60177793/91706472-13553c00-eb9c-11ea-801f-f1531483d010.png)
![image](https://user-images.githubusercontent.com/60177793/91706463-0e908800-eb9c-11ea-9d14-bac41dcce70f.png)





