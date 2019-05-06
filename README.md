# Sawtooth Event Listner in Go

## Set-up steps.

### Installation on Mac OS 10.14.4

1. Install golang 1.9 or higher
2. Set $GOPATH and $GOROOT environment variables.
3. Install Git, Python3 and Openssl
4. Using PIP, install grpcio, grpcio-tools, setuptools with --upgrade flag.
5. Install ```bash brew install pkg-config && brew install zmq ```
6. Install sawtooth go SDK ```bash go get github.com/hyperledger/sawtooth-sdk-go ```
7. Go to $GOPATH/src/github.com/hyperledger/sawtooth-sdk-go and run ```bash go generate ```
8. Copy $GOPATH/src/github.com/hyperledger/sawtooth-sdk-go/protobuf/events_pb2 to $GOPATH/src/protobuf/events_pb2

## Running the subscriber client.

Calculate the TP prefix

To run, start the validator then type the following on the command line:
	```bash go run events_subcribe_client.go ```

Note: If you're using docker-compose file default IP is already set.
Otherwise, please set global environment variable as
VALIDATOR_URL="tcp://<VALIDATOR-IP>:4004"