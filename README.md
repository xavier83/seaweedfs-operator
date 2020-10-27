# SeaweedFS Operator

Goals: 
* Automatically deploy a SeaweedFS cluster with 3 masters, N volume servers, and M filers with replicated leveldb as filer store.
* Auto rolling upgrade and restart.
* Ingress for volume server, filer and S3, to support HDFS, REST filer, S3 API and cross-cluster replication.
* Support all major cloud Kubernetes: AWS, Google, Azure.

## Installation

## Development

Follow the instructions in https://sdk.operatorframework.io/docs/building-operators/golang/quickstart/

```
$ git clone https://github.com/seaweedfs/seaweedfs-operator
$ cd seaweedfs-operator

# register the CRD with the Kubernetes
$ make install

# run the operator locally outside the Kubernetes cluster
$ make run ENABLE_WEBHOOKS=false 

# From another terminal in the same directory
$ kubectl apply -f config/samples/seaweed_v1_seaweed.yaml

```
