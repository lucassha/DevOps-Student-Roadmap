### October 2018 - Blog 4
#### Docker Compose

Bonjour! This month I decided to go a new route and make a YouTube tutorial series on Docker Compose. Last post, I mentioned a post on TravisCI 
with a Python script, but I thought this Docker Compose would line up nicely since the last post was on Docker basics.

If you do want some exposure with Docker and Travis automated deployments, I have a repo [here](https://github.com/lucassha/python-docker-travis-cd)
where I basically did what I mentioned.
I might eventually write a blog post on the process (Docker isn't technically really necessary), but it'll be some time later.

#### YouTube Link

If you don't want to read, [here's the YouTube playlist link](https://www.youtube.com/playlist?list=PLLnx2hDbasCmseHwZV34ijxxSb2Vlyxmx&disable_polymer=true),
and [here's the associated GitHub repo](https://github.com/lucassha/youtube-containers-tutorial/blob/master/README.md)

It's basically a series on building MySQL and Node.JS containers and allowing them to connect within the same network for a basic CRUD app.
Overall, Docker Compose made the networking issues of Docker substantially easier to allow containers to communicate with one another. 
For deploying apps though, an NGINX container should  be added in too in order to allow easy routing through a cloud provier.

Docker Compose seems like a great solution for smaller apps, but I definitely see Kubernetes as the future driver for apps with many, many components.
Of course, Docker Swarm may also be relatively simple, but I have very limited exposure to it.

#### Feedback

Next month, my plan is to take this same app and re-deploy it locally on Kubernetes with Minikube. Kubernetes is such a hot field at the moment,
and underlying workings of containers are really intriguing to me with control groups and namespaces. If you have thoughts on other topics, let me know! 

Until next time.
