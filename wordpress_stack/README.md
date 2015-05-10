Wordpress infrastructure using fleet and container linking, to be replaced with etcd.

To run:

```
fleetctl submit haproxy.service wordpress@.service mysql.service
fleetctl start mysql
fleetctl start wordpress@{1..4}
fleetctl start haproxy 
```

To stop:

```
fleetctl destroy haproxy wordpress@ wordpress@{1..4} mysql
```

To generate some traffic:

```
curl 127.0.0.1
```
