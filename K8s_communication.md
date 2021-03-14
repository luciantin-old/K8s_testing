# Kubernetes networking models :
- Container-to-Container communications
- Pod-to-Pod communications
- Pod-to-Service communications
- External-to-Internal/External-to-Service communications


# Container-to-Container communications :
- Shared Volumes in a Kubernetes Pod
- Inter-Process Communications (IPC)
    - SystemV semaphores
    - POSIX shared memory
    - Message Queues
    
# Pod-to-Pod communications
- DNS Records of service/pod name -> [link](https://kubernetes.io/docs/concepts/services-networking/dns-pod-service/)

# Pod-to-Service communications
- When we create a service, an endpoint object will be created, which describes a set of pod IPs that the label selector in that service has selected.
- The service IPs are assigned from a range configured in the Kubernetes API Server via the --service-ip-range flag. These are virtual IPs which are intercepted by a kube-proxy process running locally on each node. These IPs do not need to be routable off-host, because IPTables rules will intercept the traffic, and route to the proper backend (usually the pod network).
- A requirement of a manually configured network is that the service-ip-range does not conflict with existing network infrastructure.
- ?? services are only virtual and exist only to "route" traffic ??

# External-to-Internal/External-to-Service communications

- DNS with node namespace for node-to-node comm.
- 