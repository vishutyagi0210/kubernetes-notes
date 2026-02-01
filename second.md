gRPC & REST

gRPC (Google Remote Procedure Call) provides an application-level framework that allows services (usually in a private network like Kubernetes or data centers) to communicate using function calls (RPC) instead of raw HTTP endpoints.

It is built on top of:

HTTP/2 (2015)

which runs on TCP

and uses Protocol Buffers (Protobuf) for data serialization.

Timeline of HTTP and usage

HTTP/1.1 (1997)
Used mainly with REST APIs
Data formats: JSON / XML
Request style: GET /resource

HTTP/2 (2015)
Enables gRPC (RPC-style communication)
Uses Protobuf (binary format)
Faster, supports streaming and multiplexing

HTTP/3 (2023)
Runs on QUIC (UDP instead of TCP)
Focused on performance, mobile, and real-time communication
(gRPC over HTTP/3 is emerging but not yet mainstream)


master not components
1. etcd
2. kube-api-server
3. scheduler
4. controler-manager


## kube-api-server GRPC

Q/a: if our kube api server goes down.. so is our application will run?
ans: yes it will run on worker node but it will not update anything.

## work of kube-api-server workes

1. authenticatoin 
2. authorization it looks for RBAC (role base access control)
3. Admission control
3.a: validation admission control
3.b: mutating admission control: it is something which will change.
4. watch for update


# Custom-Resource-Admission
it is extending existing Kind thingi or adding new objects.

# etcd
- Distributed key value pair
- WAL ( write a head log ): when transaction happens first it consists things in WAL then it sends to disk.
- Raft Consensus
- Protobuf: used to serializing the data in binary format for fast sending.
- there is no data encryption 

q/a: how many nodes should you add to a cluster. 
ans: the best is to add odd number of nods. juski fault tolerente zyada hogi vo lo. 

# kube-scheduler
- scheduling cycle 
- bindinng cycle

# kube controller manager
it major task is to make sure that current state and state define is equals.


## worker node
major three components
- kubelet
- kube-proxy
- cri

## kube-proxy
The main task of kube-proxy is to map the ip's service and pod

Drivers: CRI (container runtime interface ) , CSI ( container storage interface ) , CNI ( container network interface ) 


Now after having all the green checks now.. kubelet came into picture

it gives signal to CRI ( container runtime interface ) then CRI can be anything like container.d , rocket , crio

then this cri do is.. it do OCI (set of parameters) has it's runc nwo CRI tells runc that create the container for me. Now it creates Cgroups [ nothing but cpu , memory ] and provide isolation. Now, it creates the container.. deployed Now, it gives it to kubelet now kubelet pass the application workload... that it happening.
runc ( solomon hikes created this )- is in GO language then beucase of limitations crun came up it created in C created by redhat

Q/a what is the difference between?  runc crun
Q/a is CRI creates the container?



