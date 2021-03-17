# K8s image creation

ex. flask hello world

- build image
``` 
docker build dir/of/Dockerfile -t luciantin/flask_tst
```

- start test image
```
docker run -d --name flask_tst -t luciantin/flask_tst
```

- enter bash
```
docker exec -it flask_tst /bin/bash
```

- get container ip addr
```
docker inspect container_name | grep IPAddress
```

- dockerfile EXPOSE cmd does not bind the port to localhost, docker run command needs the -p flag for that
```
docker run -d -p 5000:5000 --name flask_tst -t luciantin/flask_tst
```

- push docker image to docker hub
```
docker image push luciantin/flask_tst
```



