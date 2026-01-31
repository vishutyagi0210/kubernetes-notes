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

# most important 
```bash
ctr # specificely for container d 
crictl # it is beging used to talk to pod direct it works on container level
crictl pods # it returns the name of running pods
crictl ps -a # it returns the id only
crictl logs <id>

journalctl  # it gives logs from since the machine will be on.
journalctl --no-pager # it gives everything in one page
journalctl --since yesterday 
journalctl --since yesterday -o json-preety # it provide ... in json-pretty output.
```

## kubernetese release cycle. 4 month 

https://endoflife.date/kubernetes
https://kubernetes.io/releases/release/

1. feature discussion
2.  