# Three node kubernetes cluster setp on AWS cloud.
# Create infrastucure on AWS cloud.
	Build the VPC with multimple public and private subnets.
	Launch 3 ec2 instances one master node and two worker nodes.
	Create two different SG's for master and worker nodes and open inbound ports as per the documantation of the kubernetes.
# Once the infrastucure is up and running, run the cluster_step.sh on both master and worker nodes.
./cluster_step.sh

# Initialization of the cluster and installing network plug-in Weave.
./nw_initialization.sh

