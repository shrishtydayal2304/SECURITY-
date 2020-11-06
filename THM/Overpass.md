## Website
![image](https://user-images.githubusercontent.com/60177793/98360969-c042ae00-2050-11eb-8505-a826bbdac576.png)

## Scanning:
##### First scanned using Nmap and Zenmap and found http at port 80 and ssh at 22:
![image](https://user-images.githubusercontent.com/60177793/98360980-c3d63500-2050-11eb-9be8-3a80c95e97ba.png)
![image](https://user-images.githubusercontent.com/60177793/98360992-c9cc1600-2050-11eb-8c39-b69431e6ece6.png)

## Enumeration
##### I used gobuster to find the hidden directories and the result as shown: The admin page seems to be the login page and we need to find the credentials

![image](https://user-images.githubusercontent.com/60177793/98361072-e23c3080-2050-11eb-9e6e-bb1aa8e5a004.png)
![image](https://user-images.githubusercontent.com/60177793/98361086-e7997b00-2050-11eb-9b70-d39504082b8d.png)

## Hint:
##### From the hint it is clear ,its one of OWASP 10 but no brute force .So it can be sql injection or broken authentication.Inspecting the pages and cookies:

![image](https://user-images.githubusercontent.com/60177793/98361128-faac4b00-2050-11eb-95cd-edf67d0bb807.png)
##### There are 3 javascript file out of which the cookies.js and admin.js are the default one and the third one is login.js.So we can try to get the username or someusefull info:
#####  I moved on to login.js because that seemed to be custom code. Hovering through the code, the login() function caught my eye.f incorrect, it outputs “Incorrect Credentials”, but if correct, it sets a Cookie named SessionToken and redirects the user to /admin. I wonder if the server actually validates the cookie 😉
##### I  will be using the cookies editor plugin which are available for the firefox browsers:I created my own cookie using the browser extension EditThisCookie with SessionToken as the name and gave it some random value.
##### Usse the name as SessionToken as we can giver user values too:

![image](https://user-images.githubusercontent.com/60177793/98361140-00099580-2051-11eb-988a-6fb9da174083.png)
![image](https://user-images.githubusercontent.com/60177793/98361153-07c93a00-2051-11eb-8e1a-69073f516e8f.png)
![image](https://user-images.githubusercontent.com/60177793/98361162-0dbf1b00-2051-11eb-92dc-7b9239dd5c7f.png)

![image](https://user-images.githubusercontent.com/60177793/98363899-c6875900-2055-11eb-851b-5fe95f076c99.png)
##### We are greeted as the Administrator and there is a note to James. Before we go any further, there are two ways of SSH authentication:By username and password and By username and public-private keypairs.
![image](https://user-images.githubusercontent.com/60177793/98363938-d737cf00-2055-11eb-85cb-7caea0c5b511.png)
#### Next step is:In here, the private key of the user is exposed 🤦‍♂ ️. The other part i.e. the username could be easily guessed: james. The next step is trying to login through ssh. So, I copied this private key to a file and using the -i flag in ssh, I can provide the private key (usually named id_rsa)

