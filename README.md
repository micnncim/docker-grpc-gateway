# docker-grpc-gateway

Dockerfile for [grpc-gateway](https://github.com/grpc-ecosystem/grpc-gateway) and golang.

## Note

[golang/protobuf](https://github.com/golang/protobuf) has an issue: [#763](https://github.com/golang/protobuf/issues/763).  
Until the issue fixed, use [`downgrade-proto`](https://github.com/micnncim/docker-grpc-gateway/tree/downgrade-proto) branch.

## Setup

1. Replace repository owner and name.

e.g.)

```sh
$ sed -i -e 's/micnncim/<REPOSITORY_OWNER>/g' -e 's/docker-grpc-gateway/<REPOSITORY_NAME>/g' Dockerfile
```

2. Set your Dockerfile ENV: `PROTO_FILES` `PROTO_GO_OUT`

default:

```
ENV PROTO_FILES=./proto/*.proto \
    PROTO_GO_OUT=./src
```

## LICENSE

[MIT](./LICENSE)
