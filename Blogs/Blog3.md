### September 2018 - Blog 2
#### Docker - What is it & a few simple examples

Hi! For this blog, I want to discuss Docker, its uses, a practical example, and some other hypotheticals. It's really easy to get too technical with Docker,
so I'm going to try to keep it simple. 

**Here's the plan:**
 
* A bit on virtualization
* Docker vs. virtual machines
* Uses of Docker
* Dockerfile example
* Hypotheticals
* TravisCI with Docker 

Without further ado, let's get into it.

<hr>

#### Virtualization 

Ever seen the acronym VM and not known what it stands for? Well, most likely, it stands for virtual machine, which uses a hypervisor 
to allow different operating systems to run on your computer (think, running Ubuntu on the command line from your Mac operating system). 
A commonly used VM for testing is [Vagrant](https://www.vagrantup.com/) with [Virtual Box](https://www.virtualbox.org/wiki/Downloads).
Think of the hypervisor as a supervisor that manages VMs. That's pretty much it. If you wanna get into the nitty gritty, a quick 
[Google search](https://www.networkworld.com/article/3243262/virtualization/what-is-a-hypervisor.html) will bring up some good resources. 

#### Docker vs VMs

Let's take a look at this photo (courtesy of Docker) and see the difference:

![](https://imgur.com/a/yK4ZLxL)
