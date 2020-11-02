# Basic test data 


## Upstream useful images

### Docker.io



### quay.io

* quay.io/redhattraining/hello-world-nginx:v1.0


## Quick setup

### nginx hello world

```
$ oc new-project ngnix_hello_world

$ oc new-app --name nginx-hello --docker-image quay.io/redhattraining/hello-world-nginx:v1.0

$ oc create route edge --service nginx-hello --hostname nginx-hello.apps.ocp4.example.com

$ curl https://nginx-hello.apps.ocp4.example.com
<html>
  <body>
    <h1>Hello, world from nginx!</h1>
  </body>
</html>
```
