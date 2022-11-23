# Interview Questions and Model Answers

## What is Devops?

a set of practices which use tools to help the organisation deliver services at high speed. This helps organisations to automatate and integrate the process between software development and IT teams. It emphasizes team empowerment, cross-team communication and collaboration, and technology automation

---

## Benefits of Devops?

1. Faster, better product delivery due to scrum and agile methodology.
2. Fast adaptation to changes of user needs, providing a pleasent experience to the end-user
3. as automation is a key practice in devops, management and operations are easier to control and use to solve problems quicker
4. improved collaborations due to the agile methodology there is constant communication between company and client so their needs can be met

---

## What is the role of a devops engineer? 

For a junior engineer they will need to:
  - install and deploy automation tools
  - monitor code quality
  - collaborate with other team members to ensure releases happen on time

A mid level engineer will need to:
- orchestrate and debug complex software products
- write advanced automation scripts in reduced time
- predict what changing part of teh software might have on another

A senior engineer will need to:

- co ordinate teams and lead projects
- Know how to explain technical languages to business language
- negotiating with clients and stake holders 

---

## Technologies I have used:

- **Vagrant**
  - S - I had monolith app and needed to make it into a 2 tier app
  - T - convert the monolith into a 2 tier
  - A - built two vm's app and db and connecting them using db-host variable
  - R - Had successfully built a 2 Tier architecture 
- **Docker**
  - S - had a the monolith app on my local host
  - T - make to two images and automate the process of launching the 2 tier architecture
  - A - made two images of node and mongo and used docker-compose.yml file to automate the process
  - R - Had two contianers running with the run of one command and they were both linking together using the .yml file
- **Terraform**
  - S - It takes too long to make manually set up a VPC and launch an autoscalling group etc
  - T - Needed to automate building a VPC using .tf files with the correct configurations
  - A - Made multiple .tf files that automate making VPC and autoscaling groups and cloud watch and sns etc.
  - R - Was able to get the automation working using the terraform files
- **AWS**
  - S - if the cpu usage goes over 20% it is using too much power
  - T - make an autoscaling group to solve this issue
  - A - made a cloud watch to see if the cpu usage is going over 20% then that instance will get destroyed and another instance is made using the autoscalling group
  - R - successfully made the autoscalling group and cloud watch and was able to test it using an infinite loop in one of the machines
  
- **Ansible**
  - S - constantly had to rerun the machines to run provisions
  - T - needed to make playbooks to run these provisions on each vm
  - A - Made an ansible controller that holds my aws keys in a ansible vault and connects to the two vms app and db and runs the 2 tier architecture app
  - R - Was able to manage and orchestrate our code in both instances
- **GIT/GITHUB**
  - S - Wanted an update version of the code available at all times
  - T - Working on the group project we needed a version control so i had the updated version
  - A - Created a repo we can all work on. had different branches we all worked on and then at the end we merged it into one branch 
  - R - Was able to all work on three different branches front back and db and merged it midway to get it all working
- **IAC**
  - S
  - T
  - A
  - R
- **Jenkins**
  - S
  - T
  - A
  - R
  
---

## What is IaC?

Infrastructure as code is 

---

## What is Ansible?

---

## What is Terraform?

---

## Mock interview questions:

What is CI/CD?

Continuous Integration / Continuous Delivery or Deployment

CI CD is considered as the backbone of DevOps practices and automation, It plays a vital role in a business as it allows faster delivery times by automating the production process. There are 4 stages of CI/CD. these are Source, Build Test and production 

continuous integration is where the developers merge and commit the code to the shared repository frequently and have it tested and maintained. 

continuous delivery is when the testing has passed and the product is ready for production but just needs the developers approval. 

there is another aspect called continous deployment which requires no human interaction. So if the test passes it is automatically sent through production. 

What is Jenkins?

It is an open source automation server that allows an organisation to run CI/CD processes. Jenkins supports building, deploying and automating for software development projects. It is easy to install, simple to use and has a user friendly interface and used by big companies like Facebook, Netflix and Ebay.



What are the stages of software development life cycle? 

There are 7 stages of the software development life cycle. These are Requirement collection, Design, development, test, deploy and maintain.

What is VPC?

It stands for virtual private cloud and it is an isolated area in the AWS cloud that allows you to run your virtual machines with your fully customised networks and settings. 

What is the difference between security group and NACL?

security group is the security on the server/virtual machine level and NACL is the security on the subnet level.


What is Ansible and Terraform?

Ansible allows you to manage, update and reconfigure the machines that terraform creates. Terraform can be defined as a tool for versioning, changing and building infrastructure efficiently and safely


