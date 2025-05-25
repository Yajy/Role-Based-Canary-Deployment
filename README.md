# Role-Based-Canary-Deployment
Role-based canary deployment on AWS EKS using Istio. Routes traffic to Go-based backend v1/v2 based on user roles via HTTP headers. Includes Kubernetes manifests for Deployments, Services, Istio Gateway, VirtualService, and DestinationRule for safe feature rollout.
