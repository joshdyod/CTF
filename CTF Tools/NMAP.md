## NMAP ##

Check for Vulns


`nmap -sC -sV -oA hostname ip
`

`nmap -v --open -sC -T4 -oA hostname ip
`

`nmap -T4 -sC -sV -oO --open -v hostname ip
`

See if there is an NMP script

`locate .nse | grep ftp`

Read info on the script

`nmap --script-help=ftp-vsftd-backdoor.nse`

Run script

`nmap --script=ftp-vsftpd-backdoor.nse 192.168.56.102 -p 21`




