# flux-helm-k8s-setup

Demo repo showing how to use Flux v2 and install a Helm Chart

## Setup

There are some secrets and setup needed to get this repo going.

1. Clone/Fork this repo
2. Create an RG in Azure and note down the name
3. Create a GitHub secret holding an Azure Service Principal following this guide: <https://github.com/Azure/actions-workflow-samples/blob/master/assets/create-secrets-for-GitHub-workflows.md> giving it access to the RG in step 2.
4. Make sure you have a Splunk instance ready for the logs. You can create a Spunk instance using the free trial at <https://www.splunk.com/en_us/products/splunk-cloud-platform.html>.

## Workflows

[![Create AKS](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/createaks.yml/badge.svg)](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/createaks.yml)
[![Deploy to AKS](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/deploy-to-aks.yml/badge.svg)](https://github.com/fredrkl/flux-helm-k8s-setup/actions/workflows/deploy-to-aks.yml)

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
