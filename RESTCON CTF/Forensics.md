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

