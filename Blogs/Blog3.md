### September 2018 - Blog 3
#### Docker - What is it & a few simple examples

Hi! For this blog, I want to discuss Docker, its uses, a practical example, and some other hypotheticals. It's really easy to get too technical with Docker,
so I'm going to try to keep it simple. 

**Disclaimer:** There are a TON of really, really good Docker resources out there. Like, a staggering amount. Take this blog as dipping 
your toes into the Mariana Trench. This is not the tutorial you need when you inevitably forget all of the Docker CLI in, like, 3 months ;) 

<hr>

#### Here's the plan 

* [A bit on virtualization](https://github.com/lucassha/DevOps-Student-Roadmap/blob/master/Blogs/Blog3.md#virtualization)
* [Docker vs. virtual machines](https://github.com/lucassha/DevOps-Student-Roadmap/blob/master/Blogs/Blog3.md#docker-vs-vms)
* [A bit on Docker](https://github.com/lucassha/DevOps-Student-Roadmap/blob/master/Blogs/Blog3.md#docker-rundown--example)
* [VM vs. Docker Image comparison](https://github.com/lucassha/DevOps-Student-Roadmap/blob/master/Blogs/Blog3.md#memory-usage)
* [Dockerfile example](https://github.com/lucassha/DevOps-Student-Roadmap/blob/master/Blogs/Blog3.md#dockerfiles) 

Without further ado, let's get into it.

<hr>

#### Virtualization 

Ever seen the acronym VM and not known what it stands for? Well, most likely, it stands for virtual machine, which uses a hypervisor 
to allow different operating systems to run on your computer (think, running Ubuntu on the command line from your Mac operating system). 
A commonly used VM for testing is [Vagrant](https://www.vagrantup.com/) with [Virtual Box](https://www.virtualbox.org/wiki/Downloads).
Think of the hypervisor as a supervisor that manages VMs. That's pretty much it. If you wanna get into the nitty gritty, a quick 
[Google search](https://www.networkworld.com/article/3243262/virtualization/what-is-a-hypervisor.html) will bring up some good resources.

What's the purpose of VMs? Lots of reasons. It mostly boils down to isolation and utilizing resources efficiently (use up that CPU! No need to buy another server when one is barely utilized).

<hr>

#### Docker vs VMs

Let's take a look at this photo (courtesy of Docker) and see the difference:

![](https://imgur.com/p8l7dyw.png)

So, what's the difference? 

Well, Docker runs on top of your host OS. Without going too technical, Docker creates an isolated environment with namespaces, cgroups, and some filesystem manipulation (I don't totally understand either, don't worry!). 

In comparison, VMs actually install additional guest OSes on top of your own OS with the help of a hypervisor, which basically supervises them. 

Sooo.. why use Docker versus a VM? They're generally quite memory-friendly (don't use much memory -- back on that in a minute), portable, have an extensive list of [Docker Images](https://hub.docker.com/) (GitHub for Docker, essentially), and they can even run on top of VMs! 

[From this article](https://www.settlersoman.com/vms-are-houses-containers-are-apartments/), a nice analogy to think of the differences: Docker is like little apartments, whereas a VM is a house. Docker is all about isolation. 5 people may live under one roof, or you could split those people (which could be processes) into 5 different apartments and not have any family bickering ;) 

<hr>

#### Docker Rundown & Example

So far, I've only mentioned Docker Images, but they're more frequently called **containers**. What's the difference?

Well, a Docker Image is the pre-built image. When it runs, that's considered a container. That's really it. It's generally used interchangeably. I doubt anyone is gonna pull out a shamebell if you switch them.

I'll work through a practical example real quick. Let's say we want to run some code in Python 3, but we only have Python 2.7 installed locally. Well, let's build an image and then run the container!

`docker pull python` - this pulls down the latest Python image from Docker Hub

Now, let's run the image and also allow ourselves to use the REPL within the container

`docker run -it python` - this runs the image as a container. -i means interactive (basically, allow typing still). -t creates a sudo-tty (interact with your container basically). Don't worry about the extensions too much right now. 

Anyways, this will now allow you to type code into the REPL with Python 3! It's that simple. P.s.- if you're stuck in the REPL, ctrl+D might help :) 

The Docker CLI is your friend! It's generally quite easy to use and can give quite a bit of information very quickly. If you want to see the container you ran from, simply type in `docker images` to see the current images. If you want to see the specific container or re-run it, type in `docker ps -a`. Without the `-a`, you'll only see current running containers. 

I would highly, highly suggest at least running through the first couple pages of the [official Docker Get Started Guide](https://docs.docker.com/get-started/#containers-and-virtual-machines) if this is interesting.

<hr>

#### Memory Usage

I want to emphasize the memory difference of VMs versus Docker Images, so let's take a quick peek under the hood.

Vagrant VMs are generally hosted in ~/.vagrant.d, which shows one of my images below. This shows that VM is ~425MB. This can be shown by typing in `ls -alh`, which produces file sizes in human readable format.

```
-rw-------  1 shannonlucas  staff   425M Nov 12  2017 box-disk1.vmdk
```

If I type in `docker pull ubuntu` on the command line (this assumes you have installed Docker), this pulls down the `ubuntu:latest` Docker Image from Docker Hub. Afterwards, I type in `docker images`, I see similar information on the size:

```
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              cd6d8154f1e1        2 weeks ago         84.1MB
```

Around 340 MB smaller! That's a huge difference. 

Why is it so much smaller? Well, it could tons of reasons, but generally there is less config and some binary files may not exist. Binaries like `which`, `vim`, `nano` may not come pre-installed in the Ubuntu Docker Image, which saves space. Why not include them? Well, most likely because you won't need access to a shell environment! 

In fact, image can even get smaller. Alpine Docker Images exist, which remove even more excess. To specify a specific image, just add a colon to whatever image you want: `docker pull node:alpine`

<hr>

#### Dockerfiles

Want a custom image? Forget the Docker CLI from not using it? Want repeatable code? 

Well, this is where a Dockerfile comes in handy. It allows building a custom image based on specific specs. I'm going to run through a quick example, but I won't be explaining it in depth. This [best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/) link from Docker will give you way more accurate info than I could.

Now, let's run through a quick exp. Create a new directory somewhere on your filesystem (doesn't matter where). Open up a text editor, and name the file `Dockerfile`. No extension.

Now add these contents:

```
# add a comment on how to build this Dockerfile if you want
# docker build -t shannon:latest .

# grab the alpine image from dockerhub
FROM alpine
# run this command
CMD ["echo", "hi from the alpine container"]
```

So, let's build it, as I wrote in the comment: `docker build -t shannon:latest`

Type in `docker images` to see your new image:

```
REPOSITORY          TAG                 IMAGE ID            CREATED              SIZE
shannon             latest              03517edef7c3        About a minute ago   4.41MB
```

Now run that badboy:

`docker run 03517edef7c3` but really `docker run <your_generated_image_id_here>`

You'll get some output: `hi from the alpine container`

Boom. That's it. 

<hr>

#### Wrapping it up

Considering this post is already pretty long, I'm going to wrap it up here. Hopefully your head isn't spinning. 

If it isn't, maybe take a peek at this Alpine Linux Docker container being run in a web browser from another Docker container! 

https://contained.af/

Next up will probably be making a CI/CD pipeline example with Docker and TravisCI. It will push new builds every time we push changes to the master branch in GitHub. If you take a look at my repos, I already have some examples, but I'll break it down. Au revoir!
