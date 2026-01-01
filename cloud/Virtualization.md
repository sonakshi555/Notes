29 December 2025
# Server
A server is a powerful computer or software system that provides resources, data, or services (like hosting websites, managing emails, storing files) to other computers, called clients, over a network, following a client-server model. Unlike regular PCs, servers are built for continuous operation, high performance, and reliability, handling many simultaneous requests from various devices such as smartphones, desktops, and other systems.
##### Key Functions
- **Serves Content:** Delivers web pages, files, applications, and streaming media.
- **Manages Data:** Stores, processes, and protects large amounts of data.
- **Handles Requests:** Listens for requests from clients and sends back the necessary information. 
##### Types of Servers
- **Web Server:** Hosts websites and delivers web pages to browsers.
- Mail Server: Manages email traffic and storage.
- File Server: Stores and shares files across a network.
- Database Server : Stores and provides access to databases.


HP or IBM or many others company who provide physical server

Consider a scenario a company buys 3 server of size following
Server 1 : 100 GB ,100 processor (s1)
Server 2 : 50 GB ,50 processor(s2)
Server 3 : 25 GB ,25 processor(s3)
t[team]1,2,3
now the company assigned s1 to t1 , s2 to t2 and s3 to t3 
t1 uses 40GB , 40 processor
t2 uses 10 GB, 10 processor
t3 uses 5Gb , 5 Processor

so there is total large amount (60+40+20) GB and processor are wasted
In order to overcome this loss VM comes into to picture to increase EFFICIENCY.
# Virtual Machines
- logical isolation of servers
- http://geeksforgeeks.org/operating-systems/virtual-machines-in-operating-system/
- https://www.geeksforgeeks.org/system-design/hypervisor/
- https://www.geeksforgeeks.org/operating-systems/difference-between-virtualization-and-hypervisor/

# Creating virtual machines on AWS 

- Login to AWS console
- Make request to AWS for VM called EC2 instance
- In return to request, AWS sends the IP address and specifications that are required to login the VM
- request is sent to AWS EC2 API
- AWS EC2 API
- storage S3
- Volumes EBS
- Can be automate it by scripting

In order to get the expecting VM, the following criteria must be satisfied
- the request must be Valid
- then it should be Authenticated
- Authorized
Later run the scripts through :
- AWS CLI
- AWS API [ python boto3 ]
- AWS CFT [ Cloud Formation Templates ]
- Terraform : can automate the process in anywhere such as AWS, GCP and Azure
- AWS CDK [ Cloud Development Kit ]

AWS CDK is better than Terraform, if the organization is more concentrated on AWS rather others [Azure, GCP and others]

Terraform : Open source tool developed and maintained by Hashicorp company.
- it is used by many companies ,who use hybrid cloud provider like AWS, GCP others
- GCP for AI/ML stuff and AWS for VM or RDS
- To automate the processes and to increase efficiency

01-01-2026

## Creating EC2 instance

**1. Launched an EC2 Instance:**

- EC2 (Elastic Compute Cloud) is Amazon's cloud computing service
- An "instance" is essentially a virtual computer/server running in Amazon's data centers
- You chose Ubuntu as the operating system for this virtual server

**2. Using MobaXterm:**

- MobaXterm is a Windows application that provides an SSH client
- SSH (Secure Shell) is a secure way to remotely access and control your server
- You're using MobaXterm to connect from your local computer to your EC2 instance in the cloud

## How It Works

Think of it like this:

- **Your EC2 instance** = A computer sitting in Amazon's data center
- **MobaXterm** = A window on your computer that lets you control that remote computer
- **Ubuntu** = The Linux operating system running on that remote computer

## What You Can Do Now

When you connect through MobaXterm, you see a command line interface (terminal) where you can:

- Install software on your remote server
- Run applications
- Host websites
- Store and process data
- Basically anything you'd do on a regular computer, but it's running 24/7 in the cloud

**Analogy:** It's like renting a computer in a professional data center and controlling it from your laptop through a secure connection.


#ec2 #aws #mobaXterm
