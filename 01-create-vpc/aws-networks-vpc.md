<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Naeem Noor  
**Email:** naeemnoorawan23@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will dive into the core of AWS networking by creating your very own Virtual Private Cloud (VPC).

Setting up and managing a VPC is a vital skill for anyone looking to master cloud infrastructure. Today, you'll learn how to set up and configure a VPC from scratch. 

I'm doing this project to learn the AWS networking by Setting up and managing a VPC

### What is Amazon VPC?

Amazon VPC (Virtual Private Cloud) is a private, isolated section of AWS where you can run resources such as EC2 instances and databases. It is useful because it allows you to customize IP address ranges, subnets, route tables, and security settings, providing secure and scalable network infrastructure in the cloud.

In today’s project, I used Amazon VPC to set up a private network environment. I created subnets to divide the network, attached an Internet Gateway to allow internet access, and configured routing so that instances could communicate securely both internally and externally. This hands-on setup helped me understand network segmentation and cloud resource management.

### Personal reflection

This project took me about 1–2 hours to complete, including creating the VPC, subnets, Internet Gateway, and verifying connectivity.

One thing I didn’t expect in this project was how many small steps are required to make a VPC functional — such as attaching the Internet Gateway, updating route tables, and assigning public IPs. Even a tiny mistake can block connectivity, which highlighted the importance of careful planning and precise execution in cloud networking.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will Access the VPC console in AWS and create VPC.

### How VPCs work

A VPC (Virtual Private Cloud) is your own private network inside AWS where you can launch and control cloud resources like servers, databases, and storage just like a real on-premise network.

Think of a VPC as:

🏢 Your own secured data center in the cloud

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because you can launch resources immediately, without designing a network first.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

An IPv4 CIDR block defines a range of IP addresses that a network can use.

CIDR stands for Classless Inter-Domain Routing.

In simple words:

🧠 It tells you how many IP addresses are available in your network

---

## Subnets

### What I did in this step

We create subnets inside a VPC because a VPC is a large IP address space. Subnets allow us to divide this space into smaller networks to place different resources, control traffic, and apply security and routing rules more effectively.

### Creating and configuring subnets

A subnet (subnetwork) is a smaller network created inside a VPC by dividing the VPC’s IP address range into smaller parts.

In simple words:

🧠 A subnet is a portion of a VPC used to organize and control resources

### Public vs private subnets

The difference between public and private subnets is based on routing and accessibility. For a subnet to be considered public, it must have a route to an Internet Gateway in its route table, enabling inbound and outbound internet traffic. A private subnet does not have this route and remains isolated from direct internet access.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses. This setting makes sure that EC2 instances launched in this subnet are automatically assigned a public IP, so that they can access the internet and be accessed externally when required.

---

## Internet gateways

### What I did in this step

In this step, I will attach an Internet Gateway to my VPC. This allows instances in my subnets, especially public subnets, to send and receive traffic to and from the internet, enabling external connectivity.

### Setting up internet gateways

An Internet Gateway (IGW) is a gateway attached to your VPC that allows resources in your VPC to communicate with the internet.

In simple terms:

🌐 It’s a bridge between your private network (VPC) and the public internet.

Attaching an Internet Gateway to a VPC enables outbound and inbound internet traffic for subnets that have routes pointing to it.
If I missed this step, my VPC would remain isolated, and instances that need internet access for updates, downloads, or external communication would not work.

![Image](http://learn.nextwork.org/fulfilled_green_zany_carambola/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use AWS CloudShell to run AWS CLI commands to set up a VPC, subnet, and Internet Gateway. This helps me gain practical experience with cloud networking, automate network setup, and showcase my work in the project documentation.

### Exploring CloudShell and CLI

VPC resources can be created using AWS CloudShell, a browser-based shell environment preconfigured with AWS credentials and tools, so you don’t need to install anything on your computer.
The AWS CLI (Command Line Interface) is a tool that allows you to interact with AWS services programmatically, automating tasks and managing resources efficiently using commands instead of the AWS Management Console.

### Debugging my setup

To create a VPC or subnet, you can use the AWS CLI. I got an error because the CIDR block I used (10.0.0.26) is invalid — AWS requires a valid CIDR range that defines the network, such as 10.0.0.0/24 or 10.0.1.0/28. Single IP addresses cannot be used.
To avoid errors, always provide a network address with proper prefix notation when specifying a subnet.

### Comparing CloudShell vs AWS Console

---

---
