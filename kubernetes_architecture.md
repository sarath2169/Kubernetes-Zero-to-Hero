# Data Plane

## A Kubernetes worker node, also known as a minion, is responsible for running the applications in the cluster. The key components present in a Kubernetes worker node include:

### Kubelet: 
This is the primary agent that runs on each worker node. It ensures that the containers are running in a Pod as specified in the PodSpec.

### Kube-Proxy: 
This component manages network routing for the services, enabling communication between Pods and external services. It maintains network rules and handles network traffic.

### Container Runtime: 
This is the software responsible for running containers. Popular options include Docker, containerd, and CRI-O.

### Pods: 
The basic execution units in Kubernetes, which encapsulate one or more containers along with shared storage/network resources and a specification for how to run the containers.

### Node Components:
#### cAdvisor: 
Monitors resource usage and performance characteristics of running containers.
#### Log Aggregators: 
Tools like Fluentd or Logstash may be installed to collect and aggregate logs from containers.

### Networking: 
Each worker node must be connected to the cluster network to facilitate communication with other nodes and components.

> **These components work together to ensure that the applications deployed in the Kubernetes cluster are running smoothly and can scale as needed.**

# Control plane

## The Kubernetes control plane is responsible for managing the overall state of the cluster and ensuring that the desired state of the applications is maintained. The key components of the Kubernetes control plane include:

### API Server (kube-apiserver): 
The API server is the central management component that exposes the Kubernetes API. All communication with the control plane goes through the API server.

### etcd: 
This is a distributed key-value store used for storing all cluster data, including configuration data and the state of the cluster. It serves as the source of truth for the cluster.

### Controller Manager (kube-controller-manager): 
This component runs controller processes that regulate the state of the cluster. Each controller is responsible for a specific aspect of the cluster, such as node management, replication, and endpoints.

### Scheduler (kube-scheduler): 
The scheduler is responsible for assigning Pods to available nodes based on resource availability, policies, and constraints defined in the cluster.

### Cloud Controller Manager (cloud-controller-manager): 
This component interacts with cloud provider APIs to manage resources specific to the cloud environment, such as load balancers, volumes, and instances.

### Admission Controllers: 
These are plugins that govern and enforce how the API server handles requests. They can be used for various purposes, such as validating or mutating incoming requests.

> **Together, these components ensure that the cluster is running efficiently, applications are deployed correctly, and the overall system state matches the desired configuration.**
