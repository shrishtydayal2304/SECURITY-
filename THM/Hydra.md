# Hydra walkthrough
![image](https://user-images.githubusercontent.com/60177793/91703187-6d9fce00-eb97-11ea-80d0-4df5170dccc0.png)
# Task-1 Hydra Introduction
![image](https://user-images.githubusercontent.com/60177793/91703545-fb7bb900-eb97-11ea-8915-39efb8a148a8.png)
# Task-2 Using Hydra
# Use Hydra to bruteforce molly’s web password. What is flag 1?
# Answer : THM{2673a7dd116de68e85c48ec0b1f2612e}
###### Steps :This can be done by basic hydra command (hydra -l molly -P rockyou.txt http-post-form “/login:username=^USER^&password=^PASS^:incorrect” -V) as given in description

![image](https://user-images.githubusercontent.com/60177793/91704859-c40e0c00-eb99-11ea-9f7d-9c874f7a20a8.png)
![image](https://user-images.githubusercontent.com/60177793/91707205-1b61ab80-eb9d-11ea-8399-53fb78d80662.png)


![image](https://user-images.githubusercontent.com/60177793/91703909-8f4d8500-eb98-11ea-8bae-226d38ba7b0d.png)
![image](https://user-images.githubusercontent.com/60177793/91706947-bdcd5f00-eb9c-11ea-81fe-d38f1da0c369.png)
###### Now will submit the username:molly and password:sunshine on the login page and we will get the flag as shown below:

![image](https://user-images.githubusercontent.com/60177793/91707004-d3db1f80-eb9c-11ea-97e0-65bab86a51a7.png)


# 2 )Use Hydra to bruteforce molly’s SSH password. What is flag 2?
# Answer : THM{c8eeb0468febbadea859baeb33b2541b}
###### Steps: This can be done using command (hydra -l molly -P rockyou.txt ssh -V). You will get password and then login to ssh using this command (ssh molly@IP). Now ‘ls’ and ‘cat’ the flag.
![image](https://user-images.githubusercontent.com/60177793/91706358-eacd4200-eb9b-11ea-85dd-11c3fb518693.png)
###### Use the hydra command for ssh
![image](https://user-images.githubusercontent.com/60177793/91706384-f456aa00-eb9b-11ea-9b2a-4e9f1bc32e01.png)
###### Now login using ssh username@ip
![image](https://user-images.githubusercontent.com/60177793/91706472-13553c00-eb9c-11ea-801f-f1531483d010.png)

###### ls and cat to get the flag
![image](https://user-images.githubusercontent.com/60177793/91706463-0e908800-eb9c-11ea-9d14-bac41dcce70f.png)





