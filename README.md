## 1. Create a virtual host

```java
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
 }
```

### How to reload service

```
$ systemctl reload nginx
```
