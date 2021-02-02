## 1. Create a Virtual Host

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

### Inclue mine types

```java
 
 include mine.types
 
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
 }
```

## 2. Location Block

```java
 
 include mine.types
 
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
  location /great {
   return 200 "Hello World";
  }
  
 }
```

Or

```java
 
 include mine.types
 
 http {
 
  listen 80;
  server_name 167.99.93.26;
  
  root /site/demo;
  
  location = /great {
   return 200 "Hello World";
  }
  
 }
```

## 3. Variables

```java
 
 include mine.types
 
 server {
 
    http {

     if($arg_api_key != 123){
         return 401 "Incorrect API KEY";
     }
     
     listen 80;
     server_name 167.99.93.26;

     root /site/demo;

     location = /great {
      return 200 "Hello World";
     }
     
   }
   
 }
```


