# docker-elasticsearch-kubernetes

Ready to use, lean Elasticsearch Docker image ready for using within a Kubernetes cluster.

[![Docker Repository on Quay.io](https://quay.io/repository/coolpalani/docker-elasticsearch-kubernetes/status "Docker Repository on Quay.io")](https://quay.io/repository/coolpalani/docker-elasticsearch-kubernetes)

## Current software

* Alpine Linux 3.9.4
* IcedTea JRE 8u212
* Elasticsearch 7.1.0

## Run

See [coolpalani/kubernetes-elasticsearch-cluster](https://github.com/coolpalani/kubernetes-elasticsearch-cluster) for instructions on how to run, scale and use Elasticsearch on Kubernetes.

## Environment variables

This image can be configured by means of environment variables, that one can set on a `Deployment`.

Besides the [inherited ones](https://github.com/coolpalani/docker-elasticsearch#environment-variables), this container image provides the following:

* [DISCOVERY_SERVICE](https://www.elastic.co/guide/en/elasticsearch/reference/current/modules-discovery-zen.html#unicast) - the service to be queried for through DNS (default = `elasticsearch-discovery`).
* [MEMORY_LOCK](https://www.elastic.co/guide/en/elasticsearch/reference/current/important-settings.html#bootstrap.memory_lock) - memory locking control defaults to `false` as Kubernetes requires swap to be disabled.
