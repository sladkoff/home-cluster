
<img src="https://camo.githubusercontent.com/5b298bf6b0596795602bd771c5bddbb963e83e0f/68747470733a2f2f692e696d6775722e636f6d2f7031527a586a512e706e67" align="left" width="144px" height="144px"/>

### My home Kubernetes cluster :motor_boat: 
_... managed by Flux. For testing and prototyping._

<br/>
<br/>
<br/>

<br/>

## :notebook:&nbsp; Overview

This repository _is_ my homelab Kubernetes cluster in a declarative state. [Flux v2](https://github.com/fluxcd/flux2) watches my [cluster](cluster/) folder and makes the changes to my cluster based on the YAML manifests.



## :test_tube:&nbsp; "The DevOps Lab"

List of stuff I (want to) run on the cluster. Mostly for "science" and for personal satisfaction.

- :white_check_mark: [Flux v2](https://github.com/fluxcd/flux2) for declarative gitops deployments.
- :white_check_mark: [SOPS](https://github.com/mozilla/sops) for secret sharing.
- :white_check_mark: [Prometheus, Grafana](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack) and [Loki](https://github.com/grafana/loki) for monitoring.
- :white_check_mark: [Traefik](https://github.com/traefik/traefik) with automatically provisioned TLS certificates. 
- :white_check_mark: [kubeval](https://github.com/instrumenta/kubeval) and [kube-score](https://github.com/zegl/kube-score) for validating the cluster declarations.
- :negative_squared_cross_mark: [Flagger](https://github.com/fluxcd/flagger) for progressive delivery with canary deployments...
- :negative_squared_cross_mark: Ansible (with kubespray?) for provisioning the k8s cluster itself... 
- :negative_squared_cross_mark: More Github Actions for keeping things up-to-date...



## :desktop_computer:&nbsp; Cluster Setup

My single-node k8s cluster is running on old bare metal in my basement. It was set up with [kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/) on CentOS.

**TODO**: Automate the k8s installation with Ansible.



## :heart:&nbsp; Thanks

A lot of inspiration for my flux repo structure came from [onder0p's home cluster](https://github.com/onedr0p/home-cluster).
