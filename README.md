# docker_app
## wrk
### build 
```shell
docker build -t wrk .
```

### use
```shell
docker run --rm --name wrk -v `pwd`:/data -w /data -it wrk wrk -c5 -t5 -d5s -s test.lua https://www.baidu.com:443 --latency 
```
