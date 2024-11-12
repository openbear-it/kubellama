# KubeLLaMA

This repository provides a solution for deploying the [Llama language model](https://github.com/facebookresearch/llama) with [Open WebUI](https://github.com/open-webui/open-webui) on a Kubernetes (K8s) cluster. The setup includes all necessary configuration files and guides to deploy and manage the model across multiple nodes in a scalable and efficient way.

## Table of Contents
- [Overview](#overview)
- [Setup](#setup)
  - [Step 1: Clone the Repository](#step-1-clone-the-repository)
  - [Step 2: Apply Kubernetes Manifests](#step-3-apply-kubernetes-manifests)
  - [Step 3: Accessing the Open WebUI](#step-4-accessing-the-open-webui)
- [Customization](#customization)
- [Contributing](#contributing)

## Overview
Llama is a state-of-the-art open-source large language model created by Meta. With the Open WebUI, users can interact with the model through a web-based user interface. This solution allows you to deploy Llama with Open WebUI in a Kubernetes environment, making it easy to scale resources up or down as needed and manage the application through Kubernetes tools.

## Setup

### Step 1: Clone the Repository
Clone this repository to your local machine.

```bash
git clone https://github.com/openbear-it/kubellama.git
cd kubellama
```

### Step 2: Apply Kubernetes Manifests

To deploy Llama and Open WebUI on your cluster, use the following command to apply all Kubernetes manifests:
```bash
kubectl apply -f yaml/
```

### Step 3: Accessing the Open WebUI

After deployment, the Open WebUI can be accessed:
- **Via Ingress**: If you have an Ingress controller, access it through the configured hostname.

## Customization

- **Model Selection**: Update the deployment file (`yaml/deployments.yaml`) to specify the Llama model you wish to deploy.
- **Resource Limits**: Adjust CPU and memory limits in the deployment file to optimize resource allocation.


Ensure the storage solution supports simultaneous access if running multiple instances.               

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any bugs, improvements, or new feature requests.