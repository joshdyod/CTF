## Hashcat ##

`cd ~/Downloads/CTFs/`

Create hash text file

`sudo nano /hashes/hashes_CTF.txt`

Now run the Hash CMD

`hashcat -m 0 /hashes/hashes_CTF.txt -o passwords_CTF.txt rockyou.txt`