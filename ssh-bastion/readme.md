## Let's see a demo

This is a template of a ssh bastion among others internal servers that are not accesible to get connected via ssh.

![enter image description here](https://raw.githubusercontent.com/edgarleonardo/cloud_formation_examples/master/ssh-bastion/bastion.jpg)

The json template for fulfill with the image below is this:
[Cloudformation Json Template](https://github.com/edgarleonardo/cloud_formation_examples/blob/master/ssh-bastion/ssh-bastion-ec2.json)

Now let's explain the base of the json:

**AWSTemplateFormatVersion**: this is the version of the template, the only that exists is 2010-09-09.

**Mapings**: this is a place where we add constant to be used through out the template's resources.

**Resources**: Here are all AWS componenet and their interactions, cloudformation manage all dependency among components in an easy way, as we can see in the Json there are: 

 1. *VPC*: is the base of all componenets on AWS, here are located the different resources.
 2. *EC2Instance*: is the Virtual Machine that will run our node application.
 3. *InternetGateway*: is the component that allows us get to the internet.
 4. *VPCGatewayAttachment*: is the attachment between VPC and InternetGateway.
 5. *WebServerSubnet*: this is where the network is configured.
 6. *Route Table*: is the routing table that allow the comunications among componenets inside a VPC.
 7. *NetworkAcl*: is the access list that are configured to protect the access to the resource on our server.

When we finish up our template we just run the next script from the *CLI*:

> **For Creating the stack on AWS from CLI**
aws cloudformation create-stack --stack-name bastion-host-for-ssh --template-body file://ssh-bastion-ec2.json --parameters ParameterKey=VPC, ParameterValue=YOUR_VPC_ID, ParameterKey=NetworkSubnet, ParameterValue=YOU_SUBNET_ON_VPC, ParameterKey=KeyPair, ParameterValue=SSH_PUB_KEY, ParameterKey=Ec2InstanceType, ParameterValue=t2.micro

> **For checking if the stack is already created from CLI**
aws cloudformation describe-stacks

> **For Deleting the stack from CLI**
aws cloudformation delete-stack --stack-name bastion-host-for-ssh

When you create you stack, you will be able to see the components created in AWS.
