# everything in linux is a file.

command
```bash
ls ~ list the command
ls -a

ps aux ~ list down all the running processes
pstree # shows the running processes with a hirearchical view
``` 

# encodinng in base64

```bash
echo vishal | base64
echo <code> | base64 --decode
```

# reading logs 
```bash
head filename # returns first 10 lines
tail filename # returns last 10 lines
```

# network troubleshoot
```bash
tcpdump
tcpdump -c 10 # only 10 packets capture.
tcpdump -c 2 > filename # save in file these output.
tcpdump -i <interface_name> -c 2 > filename # check from a specific interface

```