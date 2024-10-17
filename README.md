# Eclipse Mosquitto MQTT Broker and Node-RED Deployment on Kubernetes

This project demonstrates the deployment of an Eclipse Mosquitto MQTT broker along with Node-RED on a Kubernetes cluster using YAML configuration files. It facilitates secure communication and provides a platform for data visualization and processing.

## Table of Contents

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [How to Run](#how-to-run)
- [Configuration Files](#configuration-files)
- [Screenshots](#screenshots)
=
## Project Overview

This project includes the necessary deployments and services to run both the Mosquitto broker and Node-RED. It also sets up a persistent volume for Node-RED to ensure data persistence.

## Project Structure

. ├── ca.crt ├── flow.json ├── node-red-deployment.yaml ├── nodered-pvc.yaml ├── server.crt ├── server.key └── screenshots


## Prerequisites

- A Kubernetes cluster (local or cloud-based)
- `kubectl` installed and configured
- Access to the Kubernetes cluster with sufficient permissions to create deployments and services

## How to Run

To deploy this project on your Kubernetes cluster, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/KhizraGhaffar/kubernetes-mosquitto.git
    cd kubernetes-mosquitto
    ```

2. Apply the persistent volume claim:
    ```bash
    kubectl apply -f nodered-pvc.yaml
    ```

3. Deploy Node-RED and the Mosquitto broker:
    ```bash
    kubectl apply -f node-red-deployment.yaml
    ```

4. Verify the deployment:
    ```bash
    kubectl get pods
    ```

5. Access the Node-RED interface via the exposed service:
    ```bash
    kubectl get services
    ```

## Screenshots
Screenshots of the deployment process and application usage can be found in the screenshots directory.
