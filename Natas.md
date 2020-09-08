# Natas -over the wire : It teaches the basics of the serverside web-security
# LEVEL 0
###### Natas Level 0
###### Username: natas0
###### Password: natas0
###### URL: http://natas0.natas.labs.overthewire.or


# LEVEL 0 -> LEVEL 1
![image](https://user-images.githubusercontent.com/60177793/92142573-ac50b500-ee31-11ea-852d-2175e21909fa.png)
###### PASS: gtVrDuiDfck831PqWsLEZy5gyDz1clto 


# level 1 -> level 2
![image](https://user-images.githubusercontent.com/60177793/92142613-becaee80-ee31-11ea-9bc9-77cc23c004b1.png)
###### here the right click was blocked, so we can use the kewyboard shortcut * ctr+u * 

![image](https://user-images.githubusercontent.com/60177793/92142712-df934400-ee31-11ea-97f9-f4740de1ba06.png)
###### pass :ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi
###### enter username and password to unlock the next level hint
![image](https://user-images.githubusercontent.com/60177793/92142982-431d7180-ee32-11ea-93d0-09c78dc407d7.png)

# level 2 ->  level 3
###### I inspected the page element as there was not on the website
![image](https://user-images.githubusercontent.com/60177793/92143835-73b1db00-ee33-11ea-87a0-bcc5e7e4b40a.png)


###### we want the credentials so we will check the user.txt :
![image](https://user-images.githubusercontent.com/60177793/92143655-33525d00-ee33-11ea-96d1-b4036af63461.png)

![image](https://user-images.githubusercontent.com/60177793/92143518-07cf7280-ee33-11ea-93be-c457c07a602e.png)
###### pass :sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
![image](https://user-images.githubusercontent.com/60177793/92144120-da36f900-ee33-11ea-8dc0-979f13fa0cb8.png)

# level 3 ->4 
######  now this time , we found nothing in the source code and inspect element except the message :
![image](https://user-images.githubusercontent.com/60177793/92145129-64cc2800-ee35-11ea-9ddb-c06f5b4553df.png)


###### so ,yes our next approch will be web directory , sometimes search engine crawlers leaves the user agent and alloweed and disallowed pages at robots.txt
###### We got one :
![image](https://user-images.githubusercontent.com/60177793/92144986-28003100-ee35-11ea-901b-caa229a28405.png)
![image](https://user-images.githubusercontent.com/60177793/92144826-e7081c80-ee34-11ea-9ba2-742a4b854e74.png)

##### And yes , again user.txt and after opening the link ,hurrah we got the pass for next level
![image](https://user-images.githubusercontent.com/60177793/92144800-dc4d8780-ee34-11ea-8801-fa88eea1f6ff.png)
###### Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ

# level 4 -> level 5
![image](https://user-images.githubusercontent.com/60177793/92145328-af4da480-ee35-11ea-80c7-02808795199c.png)
###### We change that Referer parameter value to Natas5
![image](https://user-images.githubusercontent.com/60177793/92253629-5f321900-eeed-11ea-9479-4d18866d825c.png)

###### After Forwarding the Request, we get the credentials of the user natas5.
![image](https://user-images.githubusercontent.com/60177793/92253690-74a74300-eeed-11ea-9244-72b7ec35cdb0.png)
![image](https://user-images.githubusercontent.com/60177793/92253804-99031f80-eeed-11ea-940a-f935602f8700.png)
###### pass :iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq

![image](https://user-images.githubusercontent.com/60177793/92253499-3578f200-eeed-11ea-8554-e068bf41c002.png)

# level 5 -> level 6
![image](https://user-images.githubusercontent.com/60177793/92253949-ccde4500-eeed-11ea-8950-690eb9265e65.png)
###### We capture the request in Burp Suite, here we see that there is a parameter named loggedin. It is set to 0. So we will set it to 1
![image](https://user-images.githubusercontent.com/60177793/92254046-f13a2180-eeed-11ea-9b68-45486b82d13d.png)
![image](https://user-images.githubusercontent.com/60177793/92254183-1e86cf80-eeee-11ea-969d-1800cbb90439.png)
![image](https://user-images.githubusercontent.com/60177793/92254447-889f7480-eeee-11ea-92dd-7e1cb268a269.png)
###### pass : aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1

# level 6 -> level 7
![image](https://user-images.githubusercontent.com/60177793/92255090-74a84280-eeef-11ea-89bd-69120a369940.png)
###### secret key :FOEIUWGHFEEUHOFUOIU
![image](https://user-images.githubusercontent.com/60177793/92255007-5b9f9180-eeef-11ea-820f-8a70b78ed3c5.png)

![image](https://user-images.githubusercontent.com/60177793/92254920-3dd22c80-eeef-11ea-841c-cd8832f16637.png)
![image](https://user-images.githubusercontent.com/60177793/92255260-ade0b280-eeef-11ea-9aac-ae06f39f9472.png)
![image](https://user-images.githubusercontent.com/60177793/92255352-d1a3f880-eeef-11ea-9365-a61b3e0826cb.png)
###### pass:7z3hEENjQtflzgnT29q7wAvMNfZdh0i9


# level 7 -> level 8
![image](https://user-images.githubusercontent.com/60177793/92255493-087a0e80-eef0-11ea-95a9-4c96304d512d.png)
![image](https://user-images.githubusercontent.com/60177793/92255656-4414d880-eef0-11ea-82a1-ee3d520f1d6a.png)
###### So, we modify the link to read the password stored in the natas_webpass.
###### natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8
###### And we have the password for the next level. This is called command injection.
![image](https://user-images.githubusercontent.com/60177793/92256837-d9fd3300-eef1-11ea-8293-1f095331af10.png)
###### pass: DBfUBfqQG69KvJvJ1iAbMoIpwSNQ9bWe


# level 8 -> level 9
![image](https://user-images.githubusercontent.com/60177793/92257376-bf778980-eef2-11ea-830a-3e9d45f9843a.png)

###### secret messegae can be decoded using cyberchef tools:

![image](https://user-images.githubusercontent.com/60177793/92457978-7ec58c00-f1e2-11ea-8394-f80ac5cc8859.png)
![image](https://user-images.githubusercontent.com/60177793/92458166-ae749400-f1e2-11ea-8a9f-2ba4697271b8.png)
###### pass : W0mMhUcRRnG8dcghE4qvk3JA9lGt8nDl

# level 9-> level 10
![image](https://user-images.githubusercontent.com/60177793/92458007-871dc700-f1e2-11ea-9773-89da82ae6409.png)



###### pass : nOpp1igQAkUzaI1GUUjzn1bFVj7xCNzu

# level 10->level 11
![image](https://user-images.githubusercontent.com/60177793/92503174-81de6d80-f21e-11ea-8392-fdb6f360149d.png)
![image](https://user-images.githubusercontent.com/60177793/92503313-b3573900-f21e-11ea-81e4-387354d3d2a6.png)
###### We opened the source code and found that when we enter a keyword, it is passed via a function called passthru(). It takes the value in $key and it filters the input of ###### the characters (/;|&) as shown in the given image.
###### So we can use (.*) to execute multiple commands
![image](https://user-images.githubusercontent.com/60177793/92504135-d9310d80-f21f-11ea-92cd-08a3e400d929.png)
###### pass: U82q5TCMMQ9xuFoI3dYX61s7OZD9JKoK





