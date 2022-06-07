## Take Steps To Secure Your AWS Network (AWS VPC)

This blog will give you a quick walkthrough of security groups and the network access control list (Network ACL). I will be talking about.

## What is a Security Group and Network ACL?

To improve network security we should create firewalls that will filter network connections from different IP addresses. This is what Both Security groups and Network ACL are they are virtual firewalls that deny or allow access to your resources in the virtual private cloud (VPC). They do it using different approaches.

![Alt Text](https://media.giphy.com/media/bKj0qEKTVBdF2o5Dgn/giphy.gif)

## Stateful & Stateless Firewalls (Security Group)

Understanding the difference between a stateful and a stateless firewall will save you a lot of headaches in the long run because it is one of the main differences when it comes to a security group and a Network ACL. 

### Stateful Firewall
A stateful firewall allows the inbound and outbound traffic from one connection to be defined by one rule. What do I mean by that? 🤔🤔🤔

Whenever you make a rule for a firewall I want you to think of it as if you are creating a whole to allow for network traffic to go through but the cool thing with stateful firewalls is it understands if you set inbound traffic on port 80. The outbound traffic will be handled automatically. this works both ways so for example if I allow for outbound traffic on port 22 (SSH port) the response to this traffic will be handled automatically without the need to set any extra rules.

### Stateless Firewall (Network ACL)
A stateless firewall is a firewall that is not "smart". This means you will need to define both incoming sides of the connection so that when a request comes in it will be handled by one rule and you will need to define another rule for the same connection to receive a response.

[If you are still confused check out this post for another explanation](https://www.linkedin.com/pulse/aws-stateless-vs-stateful-packet-filtering-ritesham-shastri/)

## The Difference Between Security Group & Network ACL

|  | Security Group | Network ACL |
| --- | --- | ----------- |
| Firewall Level | Instance level | Subnet level |
| Firewall Type | Stateful | Stateless |
| Deny Traffic | Implicit. by default all traffic to the security group is denied. Allow rules only.  | Explicit. The Network ACL needs to be told what traffic to allow and what traffic to deny. |
| Rule handling | All the rules are processed on each request to make sure they comply | Rules have an order to them they are processed in that order if a request meets what is set by the rule either it allows or denies the traffic the processing will be stopped at the rule. |
| Traffic Source | IP address & security group ID | IP address |

