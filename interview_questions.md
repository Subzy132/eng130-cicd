## What is DevOps? Benefits?

a set of practices which use tools to help the organisation deliver services at high speed. This helps organisations to automatate and integrate the process between software development and IT teams. It emphasizes team empowerment, cross-team communication and collaboration, and technology automation

Discuss how such an approach aims to synergize the efforts of the development and operations teams to accelerate the delivery of software products, with a minimal failure rate.

1. Faster, better product delivery due to scrum and agile methodology. 
2. Fast adaptation to changes of user needs, providing a pleasent experience to the end-user
3. as automation is a key practice in devops, management and operations are easier to control and use to solve problems quicker
4. improved collaborations due to the agile methodology there is constant communication between company and client so their needs can be met.

## What is OOP?

it is a progamming paradigm. it is very popular way of programming in recent times and it is a concept based around 'objects' and tries to mimic real-life objects behavior, storing data and functions related to them. It is used to structure a program into simple, reusable pieces of code blueprints (called classes), that are used to create individual instances of objects.

## What are the four pillars of OOP?

Encapsulation - Encapsulation is a technique of restricting a user from directly modifying the data members or variables of a class in order to maintain the integrity of the data

Polymorphism - Polymorphism literally means “many forms”. This principle focuses on designing objects to share behaviors. Building from inheritance, polymorphism allows the same method to execute different behaviors in two ways: method overriding and method overloading

Abstraction - Abstraction means that the user only interacts with selected attributes and methods of an object. It uses simple things to represent complexity, the main goal is to hide complexity details from the user. Take your phone for example, when taking a photo the user (you) only need to press a single button, however many processes are happening inside of your mobile device to process the image and render it on your screen. This information is very complex and would confuse the user so it is better kept hidden.

Inheritance - Inheritance is one of the most important aspects of OOP. It allows classes to inherit features of other classes. Put another way, parent classes extend attributes and behaviors to child classes. Inheritance supports reusability

## What are the benefits of OOP?

- implements DRY do not repeat yourself as the code can be reusable through inheritance
- effective probelm solving because you are working in chunks. you can see exaclty where the problem is. 
- It's easier to create large programs. Because OOP helps you eliminate unnecessary code, it's easier to create larger, more complex programs with OOP

## What is ansible

Ansible is an automation tool that automates cloud provisioning.

it easier to edit and distribute configurations. It also ensures that we provision the same environment every time.

It is an example of infrastructure as code which is is the managing and provisioning of infrastructure through code instead of through manual configurations.

With IaC, configuration files are created that contain our infrastructure specifications,

## What are Ad-Hoc commands

Ad hoc commands are commands which can be run individually to perform quick functions. These commands need not be performed later. Sudo ansible all -a "date"

## What does CI/CD do for the business?

CI\CD allows organisations to publish software quickly and efficiently. Due to the fact the code commited is constantly being tested and run so if they bump into any errors it won't go into production so they can go and quickly sort it. 

## What is the difference between a monolith and 2tier architecture?

A monolith architecture is when you have the application in one project. In a single solution which has all your code inside that one project. 

2 tier architecture has multiple projects linking together to make an application. 

for example we had a monlith node application that ran on prim. we had all the files running from one application called app. but we converted this into a 2 tier architecture as we added two instances. the app instance and the database instance. we then connected the two using an environement variable. we now had the application running in a 2 tier architecture. 

the benefits of this is that it is easier to maintain and support as if there are any issues with the code you can easily find where the issue is and solve it. 

## What is the difference between a security group and a NACL?

 


A security group is a stateful firewall that is attached to an instance. It controls the inbound and outbound traffic for that instance only.

A NACL (Network Access Control List) is a stateless firewall that is attached to a subnet. It controls the inbound and outbound traffic for that subnet.



## stateful vs stateless, what is the difference?



Stateful means that the firewall remembers the state of the connection. If a connection is established, the firewall will allow the return traffic. This is the default behavior of a firewall.



Stateless means that the firewall does not remember the state of the connection. If a connection is established, the firewall will not allow the return traffic. This is the default behavior of a NACL.



## What is a VPC?

Virtual private cloud 

A VPC is a virtual network in AWS. It is a logical isolation of the AWS cloud. It allows you to launch AWS resources into a virtual network that you've defined, such as Amazon EC2 instances, into your VPC. With in a VPC you can create subnets, route tables, internet gateways, and network access control lists. These all work together to provide security and network access to your instances.



Subnet - A subnet is a range of IP addresses in your VPC. You can launch your AWS resources, into a specific subnet.



Route Table - A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.



Internet Gateway - An internet gateway is a ighly available VPC component that allows communication between instances in your VPC and the internet. It is the target for the route in your route table for internet-routable traffic.



Network Access Control List - A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets. You can use network ACLs to allow or deny traffic to and from specific Amazon EC2 instances in your VPC.

## How did you make sure your app was secure on AWS? 

There are multiple ways the app is portected on AWS. With the main one being is setting the security groups. this acts as a firewall so you can set up which specific ip can access the app. if that IP is not in the security group then they won't be able to access it.

another protection is the use of ssh keys. so the way the local host is connected to the instances is using 
## What is CI/CD

CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app development. The main concepts attributed to CI/CD are continuous integration, continuous delivery, and continuous deployment.
CI – continually pushing changes to github
CD- after changes are pushed you manually build and push to production
CDE everything is automated using the webhook
Difference between delivery and deployment is on delivery the integration is automatic but you manually deploy the application whereas deployment the whole process is automated so it integrates, tests and deploys it automatically 

## Explain CI/CD process

Developers machine writes code and pushes this to a github repository using the public key
the webhook triggers a Jenkins build for that repository or you can manually trigger this build
A webhook is a API that provides data as it is happening so you get the changes immediately as they are committed rather having to frequently pulling
after this webhook is triggered, Jenkins will clone down this repository to its local workspace so the agent node where it builds the product and runs its tests 
once this build is complete, the Jenkins publishes the results and launches the app using the pem file to an aws instance if the build is successful 


## What is virtualisation?

Virtualisation is the creation of a virtual (rather than actual) version of something, such as an operating system, a server, a storage device or network resources. The benefits of virtualisation include:

Efficiency - Virtualisation allows you to run multiple virtual machines on a single physical machine. This reduces the number of physical machines required to run your applications, which reduces costs.

Scalability - Virtualisation allows you to add more resources to a virtual machine, such as CPU, memory, storage, and network, without having to add more physical resources. This allows you to scale your applications up or down as required.

Flexibility - Virtualisation allows you to move virtual machines between physical machines. This allows you to move your applications between physical machines as required.

## What is GIT/Github?

Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development, but it can be used to keep track of changes in any set of files.

I used Git to track changes in my code and to collaborate with my team members. I also used Github to store my code online so I can access it from anywhere.

## Why is python used in devops?

Python is a general purpose programming language that is used in many different areas of software development. It is used in devops because it is easy to learn, easy to read, and easy to write. It is also very powerful and can be used to automate many tasks and automation is a key part of devops.

## have you done scripting before?

Yes we have done scripting before. We created scripts to provision our infrastructure and to deploy our applications using yaml files in asible. Addiontally we created scripts to automate the deployment of our applications using Jenkins.

## What is PR (Pull Request) ?

It is a process in software development when a group of collaborators are working on a project and you are ready to add or merge your code together to the final piece. you have to pull the repository so you get the newest version of the code then you start the process of merging new code changes with the main project repository.

## What is docker and docker compose file ?

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker’s methodologies for shipping, testing, and deploying code quickly, you can significantly reduce the delay between writing code and running it in production.

a docker compose file is a yaml file which is an automation script that allows you to run multiple images at one time. if you didn't have this file you would have to run the images one by one but the containers will not be linked together. the docker compose file allows you to run one script and then have this script build as many images as you need and then connect them at the same time.

