# AMQ Streams Operator

Installs the AMQ Streams operator into all namespaces.

Current channel overlays include:
* [amq-streams-2.1.x](overlays/2.x)

## Usage

If you have cloned the `dpm-hip-gitops-catalog` repository, you can install the AMQ Streams operator based on the overlay of your choice by running from the root `gitops-catalog` directory

```
oc apply -k amq-streams-operator/operator/overlays/<channel>
```

As part of a different overlay in your own GitOps repo:

```
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization

bases:
  - alm-tfs.apps.ci.gc.ca/tfs/IRCC/Scrum/_git/dpm-hip-cluster-config/amq-streams-operator/operator/overlays/amq-streams-2.1.x?ref=main
```
