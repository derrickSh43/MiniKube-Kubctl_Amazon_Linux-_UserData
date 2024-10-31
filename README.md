# MiniKube-Kubctl_Amazon_Linux-_UserData
MiniKube&amp;Kubctl_Amazon_Linux _UserData

# Ports to Open

You’ll need the following ports for Minikube, Docker, and EC2 access:

Port 22 (SSH) - For SSH access to the instance.

Port 2376 (Docker) - Required if you need to access the Docker daemon remotely (optional).

Ports 30000-32767 (NodePort Range) - For Minikube, which opens services on these ports by default for external access.

Port 443 or 8443 (Kubernetes API) - If you plan to access the Kubernetes API directly.

You can configure these in the EC2 Security Group associated with your instance.

# How to verify installs

### Connect to your EC2 instance via SSH:
  ssh ec2-user@<your-instance-public-ip>
  
### Check Docker Installation:
  docker -v

### Then verify Docker service status:    
  sudo systemctl status docker

### Check Kubectl Installation:  
  kubectl version --client

### Check Minikube Installation:  
  minikube start -- need to do this before running your kubectl commands

### You can verify Minikube's status with:  
  minikube status

### Verify Kubernetes Cluster (Minikube) is Running:  
  kubectl get pod -A


## Minimum Recommended EC2 Instances  
...t3.small (2 vCPU, 2 GB RAM)   
...t3.medium (2 vCPU, 4 GB RAM) -- good for a single node cluster   
...t3a.medium (2 vCPU, 4 GB RAM)    



  

  


  
  





