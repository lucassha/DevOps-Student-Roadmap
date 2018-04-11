### April 2018 - Blog0
#### So... what the hell is DevOps?

*If you're a purist*, it's the ideal of deploying the code your SWEs are churning out faster and easier (think automation). 
It's a combination of [lean principles](https://en.wikipedia.org/wiki/Lean_manufacturing), which is derived from manufacturing, in combination with [agile software development](https://en.wikipedia.org/wiki/Agile_software_development).
In essence, it's a cultural movement and not a job title!

*But if you're looking for a job*, [it's definitely a job title](https://www.indeed.com/jobs?q=devops+engineer&l=New+York%2C+NY).

*And if you're a student (like me)*, it's some combination of development and operations, neither of which you totally understand at the moment!

Confused yet? You bet!

<hr>

In my (admittedly humble and naive) opinion, it boils down to this:

* Knowing how to program/code (with more focus on interpreted programming languages)
* Understanding some core principles of system administration (with more focus on Linux than Windows)
* Learning the tools that combine these two things together to create infrastructure as code which leads to automated (faster) deployment of your code

I hope this makes a little more sense than the above official definition. 
This blog's purpose is to **hopefully** clarify what DevOps is and my journey as a CS student to pursuing a job in this field. 

<hr>

#### A little about me

Currently, I'm a CS student at Oregon State, where I am about 50% through the program. I have a background and previous BS in supply chain,
but I decided to go back to school for CS after being introduced to programming.

My experience is as such:

* [Python/C++/C](https://github.com/lucassha/C)
* [Linux](https://github.com/lucassha/Linux-Notes)
* [MySQL](https://github.com/lucassha/NodeJS/tree/master/CS340-Final)
* About 50% through the AWS CSA class, which I plan on completing this month
* [A little knowledge on Ansible and configuration management](https://github.com/lucassha/Ansible-Practice)

<hr>

#### The plan 

In the end, this blog is to post about my general learnings, upload all relevant files in separate repos 
(which will be driven towards beginners because, unfortunately, I am one :p),
and hopefully outline a plan on how to learn these topics. 


One of the most overwhelming and daunting factors of DevOps is **HOW MANY TOOLS AND BUZZWORDS THERE ARE**. 

For example, let's take a look at this post from [r/devops](https://www.reddit.com/r/devops/comments/77dwxd/i_feel_dirty/), 
which is currently one of the highest upvoted posts for the year (ask for permission on this).

```
I have to confess to how dirty I feel.

I now have Jenkins (which runs on Java) that calls a Jenkinsfile (which is Groovy) 
which calls a python script (which make my skin crawl) that ingests YAML, 
then using Jinja2 string substitution from the YAML values, emits a final Dockerfile, 
a bash test script that calls Gradle, then a bash build script that does a docker build and then a docker push.

I wrote all of it. I don't think anyone should ever let me near a computer again.
```

Sooo...

1) What is Jenkins, a Jenkinsfile, and Groovy
2) Python script - phew, OK, maybe I get that one
3) YAML - uhh, file type I guess
4) Jinja string substitution?
5) Dockerfile??
6) Is this all in bash? Huh
7) WHAT IS DOCKER DOING
8) OMG what is this

The point I'm trying to make is: don't be discouraged and overwhelmed right at the start. 
Clearly, this will be a battle of endurance.
There are a ton of tools in the DevOps realm and this is an extreme example. 

<hr>

#### My plan


