# Build and Run from Source Code

You can build the Spacemesh Full Node and CLI wallet directly from source code, and run the node without installing the Spacemesh App.

> You can build on Linux or on OS X. Building on Windows 10 is not yet supported.

## Linux Notes

The Spacemesh App which includes the full p2p node and a wallet is supported on any Linux distro that supports [Electron Apps](https://electronjs.org/docs/tutorial/support).

If you are running a Linux that doesn't support Electron than you can build and run a full p2p node and a CLI wallet.

--

Follow the steps below to build the Spacemesh full node and CLI wallet directly from source code.

Alternatively, you can also download a pre-build Linux full p2p node and CLI Wallet pre-build docker image and run them using Docker. Follow the steps in [this guide](docker.md).

## Building a full p2p node

Install [Go 1.11 or later](https://golang.org/dl/) for your platform, if you haven't already.
Ensure that $GOPATH is set correctly and that the $GOPATH/bin directory appears in $PATH.

### Clone the `go-spacemesh` full node repo.

```bash
git clone git@github.com:spacemeshos/go-spacemesh.git
cd go-spacemesh
```

### Install tools required for building.

run 
    ```bash
    make install
    ```
    
or get the required libs -
* protoc (the protobuf compiler)
* protoc-gen-go
* protoc-gen-grpc-gateway
* protoc-gen-swagger

### building 

`make build` or `go build` will output `go-spacemesh` executable.
*NOTE*: `docker build -t spacemesh .` to build a docker image.

## Building the CLI Wallet

## Running the full p2p node

```./go-spacemesh```

*TODO:* write about changing important configuration

## Using the CLI Wallet

- Follow [this guide](cli_wallet.md)
