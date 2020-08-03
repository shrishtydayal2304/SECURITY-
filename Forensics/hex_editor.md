## PicoCTF 2018-HEX-EDITOR

###### First download the hex_editor.jpg and open it in the terminal.
###### So, then i tried few commands like *binwalk ,exiftool and strings,grep ,cat* and one of them worked!!!!




##### Trying different commands
![image](https://user-images.githubusercontent.com/60177793/89198286-a49bb780-d5ca-11ea-9da1-95aeca751166.png)
####### using cat command we found the flag at the end of the output
![image](https://user-images.githubusercontent.com/60177793/89198469-e593cc00-d5ca-11ea-92c9-9085eb3dcc36.png)

####### But the output using command gives a lot of junk that there is in the image.
# so we can use strings with grep and pipe the output of the strings to grep that search for some part of the flag that always in the flag like “picoCTF”
![image](https://user-images.githubusercontent.com/60177793/89198597-0eb45c80-d5cb-11ea-84b7-eae6454d592c.png)


###### submission of the flag
![image](https://user-images.githubusercontent.com/60177793/89198009-293a0600-d5ca-11ea-9925-d3b7e6cf17fa.png)



