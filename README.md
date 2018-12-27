# docker-grpc-gateway

Dockerfile for [grpc-gateway](https://github.com/grpc-ecosystem/grpc-gateway).

## Note

[golang/protobuf](https://github.com/golang/protobuf) has an issue: [#763](https://github.com/golang/protobuf/issues/763).  
Until the issue fixed, use `` branch.

## Setup

1. Replace repository owner and name.

e.g.)

```sh
$ sed -i -e 's/arriv/micnncim/g' -e 's/gilgamesh-api/docker-grpc-gateway/g' Dockerfile
```

1. Set your Dockerfile ENV: `PROTO_API_FILES` `PROTO_GO_OUT`

default:

```
ENV PROTO_API_FILES=./proto/api/*.proto \
    PROTO_GO_OUT=./src
```

## LICENSE

[MIT](./LICENSE)
