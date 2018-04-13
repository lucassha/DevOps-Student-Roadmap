### April 2018 - Blog0
#### So... what the hell is DevOps?

*If you're a purist*, it's the ideal of deploying the code your SWEs are churning out faster and easier (think automation). 
It's a combination of [lean principles](https://en.wikipedia.org/wiki/Lean_manufacturing), which is derived from manufacturing, and [agile software development](https://en.wikipedia.org/wiki/Agile_software_development).
In essence, it's a cultural movement and not a job title!

*But if you're looking for a job*, [it's definitely a job title](https://www.indeed.com/jobs?q=devops+engineer&l=New+York%2C+NY).

*And if you're a student (like me)*, it's some combination of development and operations, neither of which you totally understand at the moment!

*Finally, if you're looking for an exact definition*, I like this [Shippable article](http://blog.shippable.com/how-to-be-a-great-devops-engineer):
The goal of DevOps is to ensure frequent, predictable, error-free software releases that helps you innovate faster.

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

My experience is as follows:

* [Python/C++/C](https://github.com/lucassha/C)
* [Linux](https://github.com/lucassha/Linux-Notes)
* [MySQL](https://github.com/lucassha/NodeJS/tree/master/CS340-Final)
* About 50% through the AWS CSA class, which I plan on completing this month
* [A little knowledge on Ansible and configuration management](https://github.com/lucassha/Ansible-Practice)

<hr>

#### The plan 

In the end, the purpose of this blog is to post about my general learnings, upload all relevant files in separate repos 
(which will be driven towards beginners because, as you now know, I am one :p),
and hopefully outline a plan on how to learn these topics. 


One of the most overwhelming and daunting factors of DevOps is **HOW MANY TOOLS AND BUZZWORDS THERE ARE**. 

For example, let's take a look at this post from [r/devops (courtesy of u/StephanXX)](https://www.reddit.com/r/devops/comments/77dwxd/i_feel_dirty/), 
which is currently one of the highest upvoted posts for the year.

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
3) YAML - uhh, file type specifically for parsing Python (maybe?)
4) Jinja string substitution?
5) Dockerfile??
6) Is this all in bash? Huh
7) WHAT IS DOCKER DOING
8) OMG what is this

The point I'm trying to make is: don't be discouraged and overwhelmed right at the start. 
Clearly, this will be a battle of endurance and attrition.
There are a ton of tools in the DevOps realm and this is an extreme example. 

We'll deep dive on tons of these areas including (but not limited to) configuration management tools (Ansible, Puppet, Chef), container services and virtualization (Docker, Kubernetes), scripting (Python and Bash mostly), monitoring, CI/CD, and a whole bunch of other confusing, interesting stuff!

<hr>

#### My plan

Given I already have some exposure to DevOps related tools/tasks, my plan is as follows for April:

1) Finish reading the **[Phoenix Project]**(https://www.amazon.com/Phoenix-Project-DevOps-Helping-Business/dp/0988262509), aka the quintessential DevOps book. According to pretty much everyone (aka Reddit), this should be your first step. As mentioned at the beginning of the post, DevOps is a philosophy. This book will introduce these concepts.
2) Continue learning **system administration** topics through [Linux Academy](https://linuxacademy.com/) -- I promise this isn't a sponsored plug! 
Learning bash and the CLI is crucial for so many of these tools (I'll have a successive post on this), 
and honestly this site is probably one of the best places for it.
3) Finish up the **AWS CSA** training course on both Linux Academy and [Cloud Academy](https://cloudacademy.com/dashboard/).
While the CSA in itself is not THAT useful, AWS is very in demand and DevOps is quite frequently paired with cloud infrastructure.
Most CS students have relatively little background/understanding about it, so it might give you a leg up (or at the very least show initiative)
4) Continue to learn **Python scripting**. Once again, focus is on CLI. Python is also an object-oriented language, but it's not super important for scripting. Some good resources to start would be [Learn Python the Hard Way](https://learnpythonthehardway.org/), [Colt Steele's Python Bootcamp](https://www.udemy.com/the-modern-python3-bootcamp/) (do note this is Python 3 and not 2, which can make a big difference dependent upon the tools you are using), and [Codecademy](https://www.codecademy.com/learn/learn-python) isn't half bad either. It might be a little dry in comparison to the other two though.

<hr>

#### What's next?

I'm cutting this one short because, at the moment, it's a little all over the place. 

My plan for the next blog is either to focus on **Linux CLI**, **configuration management tools**, or disecting the **Phoenix Project** with my learnings. If technical, it will be super introductory because I'm also learning these topics! And if you're one of the people actually reading this, feel free to reach out on questions/ideas/topics!
