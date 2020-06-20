# K8s Monitoring Examples
This repository contains examples to understand monitoring setup in kubernetes. We are using [Prometheus](https://prometheus.io/) for monitoring

## Setup:

We use [prometheus operator](https://github.com/coreos/prometheus-operator) for installing prometheus in kubernetes. Manifests for the setup is found in [kube-prometheus](https://github.com/coreos/kube-prometheus) project

```bash
git clone git@github.com:coreos/kube-prometheus.git

cd kube-prometheus

kubectl apply -f manifests/setup
kubectl apply -f manifests
```

## postgresql with exporter

```bash
kubectl apply -f postgres/db

kubectl apply -f postgres/exporter

kubectl apply -f postgres/servicemonitor
```