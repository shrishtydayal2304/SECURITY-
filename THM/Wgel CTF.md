# Wgel CTF
##### start with namp 
##### command : nmap -sC -sV <ipaddress>

![image](https://user-images.githubusercontent.com/60177793/94951099-55f29700-0501-11eb-9866-e7725ffee04a.png)
###### we got to know that there are 2 ports open which are 80 and 22 .
![image](https://user-images.githubusercontent.com/60177793/94951515-0eb8d600-0502-11eb-9e80-a1a7d01708be.png)
![image](https://user-images.githubusercontent.com/60177793/94951493-019be700-0502-11eb-89c7-eacc7fbab856.png)
![image](https://user-images.githubusercontent.com/60177793/94951721-7111d680-0502-11eb-9f1b-725ad2df0cd3.png)

###### now to bruteforce or check the web directory ,I will use gobuster
![image](https://user-images.githubusercontent.com/60177793/94951616-4031a180-0502-11eb-981c-847843ebb6f5.png)
![image](https://user-images.githubusercontent.com/60177793/94951681-5e979d00-0502-11eb-8422-1a72f0f26d32.png)
###### . i got something but not sure what it was so quickly i had serched some common extensions like robots.txt and some more but i did not get any sought of information 
##### then i found this 
![image](https://user-images.githubusercontent.com/60177793/94951750-7c650200-0502-11eb-806a-7ebe16c01ad4.png)
##### but not usefull so i had again run the gobuster with common wordlist
![image](https://user-images.githubusercontent.com/60177793/94951904-b6ce9f00-0502-11eb-8bfa-8c63295474c6.png)
![image](https://user-images.githubusercontent.com/60177793/94951927-bfbf7080-0502-11eb-94b7-4586bea7261d.png)
![image](https://user-images.githubusercontent.com/60177793/94951959-cf3eb980-0502-11eb-80e6-46b425696010.png)


# Now if remember something at starting of this we had an ssh connection possible. and from the source code of the first web page we found an user name called jessie:-
![image](https://user-images.githubusercontent.com/60177793/94952354-791e4600-0503-11eb-89e1-2b3f0c7a3651.png)
##### now we need to give proper permissions to execute the file
![image](https://user-images.githubusercontent.com/60177793/94952456-a5d25d80-0503-11eb-87ca-b2463ba29ab7.png)
![image](https://user-images.githubusercontent.com/60177793/94952480-b1be1f80-0503-11eb-997b-069af1abba42.png)
![image](https://user-images.githubusercontent.com/60177793/94952557-c8fd0d00-0503-11eb-844e-37874232fe68.png)

![image](https://user-images.githubusercontent.com/60177793/94952519-bbe01e00-0503-11eb-9d7a-69a61e1d7eae.png)






