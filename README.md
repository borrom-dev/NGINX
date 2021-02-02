## 1. Create a virtual host

```java
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
 }
```
### How to reload service

```java
$ systemctl reload nginx
```

### Verify config

```java
$ nginx -t
```

### Mine types


```java
 
 types {
  text/html html
  text/css css
 }
 
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
 }
```
