# Terraform-VPC-3 tier-architecture
These set of Terraform manifests show the representation of a VPC multi tier architecture in the .tf files and the terraform state files

A NAT gateway is installed in one of the public subnets to provide internet acces to systems in an unrountable CIDR range. Routing is given to the DB's in the private subnets to the NAT Gateway.

An Internet gateway is also added to give public internet access to other systems that will be installed (EC2 instances) and routing is given to the public instances to route through the Internet gateway, as their default route.

