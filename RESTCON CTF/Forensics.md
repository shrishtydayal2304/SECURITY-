#MAGIC : 1
20
File

###### NOTE: FLAG IS IN PLAIN TEXT

After scanning the qr code we get the output as:
# RESTCON{29a9df89e2858e5a25c83b6a00352d19}
![image](https://user-images.githubusercontent.com/60177793/91631901-bff7b800-e9fa-11ea-85e1-853a0e4c26e4.png)
###### Now we will try to crack this hash using crack station: https://crackstation.net/
![image](https://user-images.githubusercontent.com/60177793/91631834-59729a00-e9fa-11ea-9029-e4565694005a.png)


# Dance Monkey:
##### FIND THE HIDDEN FLAG
##### A gif is attached. If you try to do inspect element and more nothing will be found. We can try some stegnography techniques.
##### So using exiftool , we find some encoded text:
# KJCVGVCDJ5HHWU2NJFGDGX2MEFFTGXZUL5GTATSLGNMX2=== (which is base 32)
##### crack it using online tool :https://cryptii.com/
![image](https://user-images.githubusercontent.com/60177793/91632032-b458c100-e9fb-11ea-8144-9732b550e8d4.png)
# flag : RESTCON{SMIL3_L!K3_4_M0NK3Y}

###### It says cat has eaten the flag it means it is hidden somewhere and is in the file.
###### It is a png fil and we can use stego tool zsteg for that:  zsteg filename
# Flag : RESTCON{1_eaten_Y0ur_Fl4g}

# Binod
###### Hey there, we recently came to know that a malware has spread across our network ever since Binod helped one of our Desk support team by giving an employee some malicious file.Your task is to check out this program and find out the flag , remember don't believe what you see.

# I will use packet analyser tool wireshark:
![image](https://user-images.githubusercontent.com/60177793/91632517-f800fa00-e9fe-11ea-8069-29b51a576b18.png)
 ##### follow>tcp stream
![image](https://user-images.githubusercontent.com/60177793/91632532-0ea75100-e9ff-11ea-9a4b-0f887d8c53b6.png)
#####  I have exported a pdf file using wireshark through File > export object > http > binod.exe
##### which was a pdf file
![image](https://user-images.githubusercontent.com/60177793/91632557-2b438900-e9ff-11ea-9379-2e6b521d69b9.png)
###### After opening the file in visual studio code(we can use other text editor too , i noticed that there is an javascript object and there is some hex content
![image](https://user-images.githubusercontent.com/60177793/91632688-187d8400-ea00-11ea-9b1f-0480a2d85020.png)

##### used hex to ascii :https://www.rapidtables.com/convert/number/hex-to-ascii.html
![image](https://user-images.githubusercontent.com/60177793/91632642-d6544280-e9ff-11ea-9f9c-c1457a017d1d.png)
