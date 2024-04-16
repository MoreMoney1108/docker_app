# docker_app
## wrk
### build 
```shell
docker build -t wrk ./wrk_Dockerfile
```

### use
```shell
docker run --rm --name wrk -v `pwd`:/data -w /data -it wrk wrk -c5 -t5 -d5s -s test.lua https://www.baidu.com:443 --latency 
```

## protoc
### pull
```shell
docker pull rvolosatovs/protoc
```

### use
```shell
docker run --rm -v "$(pwd):/work" -w /work rvolosatovs/protoc -I=. --go_out=. --go-grpc_out=. ./foo.proto
```

## redoc
### pull
```shell
docker pull redocly/cli 
```

### use
```shell
docker run --rm -v "$(pwd):/work" -w /work redocly/cli build-docs -o index.html ./swagger.yaml
```
