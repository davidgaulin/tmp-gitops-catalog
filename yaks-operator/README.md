# OpenShift Elasticsearch Operator

Installs the Yaks operator.

Do not use the `base` directory directly, as you will need to patch the `channel` based on the version of the operator you want to use.

The current *overlays* available are for the following channels:
* [alpha](overlays/alpha)

## Usage

If you have cloned the `gitops-catalog` repository, you can install the operator based on the overlay of your choice by running from the root `gitops-catalog` directory

```
oc apply -k yaks-operator/overlays/<channel>
```