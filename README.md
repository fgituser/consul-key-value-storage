## Consul-key-value-storage

Running consul as a key value store.   
The consul API is accessed by HTTP Basic Authentication NGINX
http://localhost:8080
   
Access to API and UI default:   
login: admin   
pwd: admin   


Generating a new user   
```
htpasswd -c ./htpasswd someuser
```

Change the environment variable to your data HTPASSWD   
Additional infro from NGINX IMAGE in repo   
https://github.com/fgituser/docker-nginx-basic-auth

Request from consul API (early created key hello):
```
curl -u admin:admin -XGET http://localhost:8080/v1/kv/hello
[{"LockIndex":0,"Key":"hello","Flags":0,"Value":"ewogICJuYW1lIjogIndvcmxkIgp9","CreateIndex":28,"ModifyIndex":33}]
```


