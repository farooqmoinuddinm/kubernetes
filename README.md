# Three node kubernetes cluster setup on AWS cloud.
# Create infrastucure on AWS cloud.
	Build the VPC with multimple public and private subnets.
	Launch 3 ec2 instances one master node and two worker nodes.
	Create two different SG's for master and worker nodes and open inbound ports as per the documantation of the kubernetes.
	https://kubernetes.io/docs/reference/ports-and-protocols/
# Setup the hostname for the ec2 instances
	sudo hostnamectl set-hostname master
	sudo hostnamectl set-hostname worker1
	sudo hostnamectl set-hostname worker2
# Once the infrastucure is up and running, run the cluster_setup.sh on both master and worker nodes.
./cluster_setup.sh

# Initialization of the cluster and installing network plug-in Weave only on the master node.
./nw_initialization.sh

