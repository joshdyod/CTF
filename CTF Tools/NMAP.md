## NMAP ##

Check for Vulns

`nmap -sV -A TARGETIP`

See if there is an NMP script

`locate .nse | grep ftp`

Read info on the script

`nmap --script-help=ftp-vsftd-backdoor.nse`

Run script

`nmap --script=ftp-vsftpd-backdoor.nse 192.168.56.102 -p 21`




