## PCAP Tools ##

Snoop file

`strings capture.pcap | grep -i flag`

[[Scan For Hidden Files]]

tshark

*extract files*
`tshark -nr capture.pcap --export-objects smb,./`

*Examining HTTP traffic metadata*

`tshark -r capture.pcap -q -z http,tree`

*some of the specific fields for odd HTTP Headers*

`tshark -r capture.pcap -Y http.request -T fields -e http.host -e http.user_agent`


Use Scapy 

`#!/usr/bin/env python

from scapy.all import *

packets = rdpcap('the.pcap')

with open('out.raw', 'wb') as f:
    for p in packets:
        if UDP in p:
            chunk = bytes(p[Raw])
            f.write(chunk)`