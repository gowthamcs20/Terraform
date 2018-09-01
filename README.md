# Terraform
Terraform Practice
Installation of terraform and Creating an EC2 Instance from Terraform

#Installation: 

cd /usr/local/src

wget https://releases.hashicorp.com/terraform/0.11.8/terraform_0.11.8_linux_amd64.zip

unzip https://releases.hashicorp.com/terraform/0.11.8/terraform_0.11.8_linux_amd64.zip

mv terraform /usr/local/bin/
 
export PATH=$PATH:/terraform-path/

then verify installation :

$terraform

then 

$terraforminit

======================================================================
Using terraform to create an EC2 Instance:

After crating an AMI user with Access Key and Secret Key 

--> Create a directory named Terraform

$cd

mkdir terraform

cd terraform/

vi aws.tf


vi aws.tf

provider "aws" 
{
access_key = "abc"
secret_key = "abc"
region = "ap-southeast-1"
}

resource "aws_instance" "example" 
{
ami = "ami-83a713e0"
instance_type = "t2.micro"
tags {
Name = "Done_by_Terraform"
}
}

=================================================================

$terraform plan

$terraform apply
