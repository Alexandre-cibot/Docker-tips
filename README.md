# Docker-tips
Some usefull Docker commands


* __Remove all \<none> images__
  
```
docker rm $(docker images -f "dangling=true" -q)
```

* __Clear contairers history (old containers)__
```
docker rm $(docker ps -a -q)
```

* __Clear images and history images__
```
docker rmi $(docker images -a -q)
```

* __Filter (eg: all exited container)__
```
docker ps --filter "status=exited"

