Q/A: is worker node current running version should be greater than the master node??
Q/A: Can we use latest tags?? in our images?


command: kind create cluster --name demo --config conf.yml

# Docker
in docerk every command 
-RUN
-COPY
creates an layer and zyada layer mtlb image up maye time lagega aur isme time lagega so, pod ko up aane maye time lagega aur usse time vo image queue maye rahegi and paise jayega.


# commands
alias k-kubectl

k get nodes

<!-- more describe -->
k get nodes -o wide

k get events

<!-- tell every resource in kube  -->
kubectl api-resources

<!-- running pod -->
kubectl run name --image image:tag -- sleep 1d

<!--  for debuggin the pod -->

k get pods -o wide

k edit pod amit

<!-- apply -->
k apply -f 

<!-- go insite pod -->
k exec -it nginx -- bash

# efimeral containers
k debug  it name --image image --target name -- bash

# copy
kubectl debug myapp --image nginx --share-process --copy-to myapp-debug

# dry run
kubectl run name --image image --dry-run=client -o yaml