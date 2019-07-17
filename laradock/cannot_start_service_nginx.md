
# Cannot start service nginx

```
ERROR: for laradock_nginx_1  Cannot start service nginx: driver failed programming external connectivity on endpoint laradock_nginx_1 (ba9525ed036023164cd03be66ee381ba5f1ddd06eefec39b52c4260fa1717b92): Error starting userland proxy: Bind for 0.0.0.0:80: unexpected error (Failure EADDRINUSE)
```


### see port usage
```
sudo lsof -i :80
```
Example: In case it was the default apache on MAC using it:

1

```
sudo killall httpd
```

2
```
sudo launchctl unload /System/Library/LaunchDaemons/org.apache.httpd.plist
```

DONE

@reference: [https://github.com/laradock/laradock/issues/251](https://github.com/laradock/laradock/issues/251)
