Used for https://sysdig.com/coreos-sysdig-part-1-digging-into-coreos-environments/

After spinning up at least one balancer and one frontend using the two cloud-config files, run with:

```
fleetctl start haproxy-confd
fleetctl start frontend@{1..4}
```

And generate some traffic with:

```
curl -H 'Host:myapp.org' localhost:8080
```
