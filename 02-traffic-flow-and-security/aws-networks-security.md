<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-security)

**Author:** Naeem Noor  
**Email:** naeemnoorawan23@gmail.com

---

## VPC Traffic Flow and Security

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a private, isolated network within AWS that lets you control the network environment for your resources. It is useful because it provides customizable IP address ranges, subnets, route tables, security groups, and network gateways, allowing you to securely deploy applications and manage traffic within your cloud infrastructure.

### How I used Amazon VPC in this project

In today’s project, I used Amazon VPC to build a fully functional network environment, including public and private subnets, an Internet Gateway, route tables, security groups, and a network ACL. By doing this, I was able to practice controlling traffic flow, managing security at both instance and subnet levels, and understanding how AWS resources communicate within a VPC.

### One thing I didn't expect in this project was...

One thing I didn’t expect was how seamless it is to deploy and manage VPC resources using the AWS CLI and multi-region capabilities. I was impressed by how quickly I could create subnets, attach an Internet Gateway, configure route tables, and set up security rules, all while documenting the workflow for future reference. This gave me a new perspective on automation, efficiency, and best practices in cloud networking.

### This project took me...

This project took me approximately 3–4 hours to complete, including creating the VPC, subnets, Internet Gateway, route tables, security groups, and network ACL. The extra time was spent learning the underlying concepts and theory to ensure I fully understand how each component works within a VPC.

---

## Route tables

Route tables are a set of rules (routes) that determine where network traffic is directed within a VPC.

In simple words:

🧭 They tell traffic where to go

You need a route table to make a subnet public because route tables define where network traffic goes. Without a route directing internet-bound traffic to an Internet Gateway, resources in the subnet cannot reach the internet, even if an Internet Gateway is attached to the VPC.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

In a route table:

Destination defines where the traffic is going

Target defines where the traffic should be sent

In simple terms:

🧭 Destination = “Which traffic?”
🎯 Target = “Send it where?”

The route in my route table that directed internet-bound traffic to my Internet Gateway had a destination of 0.0.0.0/0, which represents all external traffic, and a target of the Internet Gateway, enabling internet access for resources in the public subnet.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are virtual firewalls that control inbound and outbound traffic for resources like EC2 instances inside a VPC.

In simple words:

🛡️ They decide who can talk to your instance and how

### Inbound vs Outbound rules

Inbound rules are security group rules that permit specific types of incoming network traffic to reach the instances. For my security group, I configured an inbound rule to allow HTTP traffic on port 80 from any IP address, ensuring that users can connect to the web service hosted on the instance.

Outbound rules are rules in a security group that control the types of traffic that instances can send to other resources or the internet. In my security group, the default outbound rule allows all traffic to all destinations, providing unrestricted outbound connectivity while maintaining control over inbound traffic.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are stateless virtual firewalls at the subnet level that control inbound and outbound traffic for all resources in a subnet.

In simple words:

🛡️ They control who can enter or leave a subnet, regardless of individual instances.

### Security groups vs. network ACLs

Security Groups are stateful firewalls applied to individual instances that allow only traffic you explicitly permit. Network ACLs are stateless firewalls applied at the subnet level, which can explicitly allow or deny traffic. Using both together provides layered security in a VPC.

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

The default network ACL in AWS has rules that allow all inbound and outbound traffic. Inbound rules allow any traffic from any source, and outbound rules allow traffic to any destination. This ensures that new subnets are fully functional immediately, and restrictions can be added later if needed.

A custom network ACL’s inbound and outbound rules provide fine-grained control over subnet-level traffic. You can allow or deny specific IP addresses, protocols, and port ranges. Inbound rules govern traffic entering the subnet, and outbound rules govern traffic leaving it, providing an additional security layer beyond security groups.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

In this step, I deployed three resources in a new region: a VPC, an Internet Gateway, and a Security Group. Instead of using my default AWS region, I chose us-east-1. Organizations use multiple regions to distribute workloads globally, increase redundancy, minimize latency for users, and provide backup in case of regional outages.

EC2 Global View is a tool that lets you see all your EC2 resources, including VPCs, subnets, Internet Gateways, security groups, and instances, across all AWS regions. I could even narrow down my search by resource type, region, or assigned tags, making it easy to find specific resources quickly. Without EC2 Global View, you'd have to log into each region separately and check each resource individually, which is inefficient and increases the risk of missing resources.

EC2 Global View is useful when I want to track VPCs, subnets, Internet Gateways, security groups, and EC2 instances across all regions. I would use it to identify unused resources, check global deployments, and ensure infrastructure is organized and compliant.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-security_b03ea6162)

---

---
