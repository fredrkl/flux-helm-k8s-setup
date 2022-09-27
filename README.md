# Splunk Connector setup with Flux and Helm

Demo repo showing how to use Flux v2 and install the _Splunk Connector_ Helm Chart.

## Setup

There are some secrets and setup needed to get this repo going.

1. Clone/Fork this repo
2. Create an RG in Azure and note down the name
3. Create a GitHub secret holding an Azure Service Principal following this guide: <https://github.com/Azure/actions-workflow-samples/blob/master/assets/create-secrets-for-GitHub-workflows.md> giving it access to the RG in step 2.
4. Make sure you have a Splunk instance ready for the logs. You can create a Spunk instance using the free trial at <https://www.splunk.com/en_us/products/splunk-cloud-platform.html>.
5. Update the URL in the file: <https://github.com/fredrkl/flux-helm-k8s-setup/blob/bc2488b6c284d4844d0a571037af2c59f9d1bfd6/yaml/syncfolder/splunk-connector-release.yaml#L20>

## Lessons Learned

- If you are running in a K8s cluster that is not using Docker, i.e., a type of CRI _container runtime_, then you need to set the container log format type to _cri_.
- If you are connecting to the Splunk Cloud _trial__, then you need the _insecure_ setting: <https://github.com/fredrkl/flux-helm-k8s-setup/blob/bc2488b6c284d4844d0a571037af2c59f9d1bfd6/yaml/syncfolder/splunk-connector-release.yaml#L23> Splunk Cloud Trial uses self-signed certificates.

![Splunk](./images/splunk-cloud.png)

## Workflows

[![Create AKS](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/createaks.yml/badge.svg)](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/createaks.yml)
[![Deploy to AKS](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/deploy-to-aks.yml/badge.svg)](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/deploy-to-aks.yml)

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
