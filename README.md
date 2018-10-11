# multiclusterdns
Test repository for changing API type of MultiClusterServiceDNSRecord to ServiceDNS

Example used to test the pluralization:

```
apiVersion: mygroup.k8s.io/v1beta1
kind: ServiceDNS
metadata:
  name: test-servicedns
  namespace: test-namespace
spec:
  federationName: federation-cluster
  dnsSuffix: abc.net
  
```
Results:

```
$ kubectl get servicedns
NAME               CREATED AT
test-servicedns     21m

$ kubectl get servicednss
NAME               CREATED AT
test-servicedns     21m

$ kubectl get servicednsses
error: the server doesn't have a resource type "servicednsses"


```
