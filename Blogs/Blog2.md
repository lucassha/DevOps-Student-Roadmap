### September 2018 - Blog 2
#### DevOps Internship

Hi everyone, welcome back! I just finished up my internship a couple weeks back working on the Build and Release Engineering team at a local company in Portland, OR
and thought it would be a good time to write about my experience. 
What a DevOps internship entails (anecdotal, of course!), where to focus some free time, 
and probably just some general rambling about this. 

I'll be writing about my job linearly. 

Let's dig in!

<hr>

#### The interview

For the first time in a tech interview, I REALLY enjoyed myself. It was not a coding centric or behavioral focused interview. Rather, we sat down,
talked about my interests in DevOps, Linux, (I had listed Ansible and Linux as a skill on my CV) and overall schooling. 
Because I had listed my GitHub, they just perused through random repos looking at my code and documentation. 
A couple things popped out:

* [I had an interest in Linux sys admin topics](https://github.com/lucassha/Linux-Notes)
* [I had a bit of exposure in Ansible and could at least document stuff relatively well](https://github.com/lucassha/Ansible-Practice)

This brings me to my first point in this blog:

1. Put your damn GitHub profile on your resume!

Without it, employers have no idea if you can code or where your interests lie. GH is really meant for SCM, but you can get away putting notes
and documentation on it no problem (hint hint - these posts)! This tip might seem obvious if you're reading this on GitHub, but I really want to emphasize it. Plus, you might get out of whiteboarding too ;)

In the end, they told me I was accepted for the position because I had a budding interest in Linux and DevOps, 
which put me over the top compared to other candidates that were focused on getting a SWE position.

<hr>

#### The start

Within the first week, I realized how *much* went into a CI/CD pipeline and how no Hackernoon article is going to even semi expose me 
to these things. Different production environments, a pipeline with code coverage checks written in a JVM language, deploy and release software, both Windows and Linux 
servers. Inner me was going "Holy shit, how do I learn all of this in 10 weeks." Of course, that's pretty much impossible, as I realized by 
the end of the summer, which brings me to point number two:

2. Don't try to learn everything! 

Basically the first two weeks of the job were me piddling around in Confluence documentation and looking at pipeline code having ZERO idea 
how it all came together. If I had focused on a specific area, it would have been far more valuable. In 10 weeks, you just simply don't have time. 


#### Projects

After a bunch of self-studying Linux, it became soberingly clear that I was still nowhere near competent to call myself a full-fledged
Build and Release Engineer, so with that in mind, I was assigned a couple projects that were development oriented in order to bridge the gap 
between our BRE (Build and Rel Eng) team and various teams of developers. 

**First project:** 

Develop a tool using Python (Flask as the framework) that will allow temporary access to our internal GitHub repositories for a specific team and period of time. 
In my opinion, it was the perfect first project. It allowed me to gain exposure with CRON jobs, object-relational mapping in SQL (specifically, SQLAlchemy), 
hashing database pws, Git, and code reviews in Python (whew, that's an eye opener at first). 
Speaking of code review, I want to bring up point number three:

3. You're a noob. Don't take it personally.

The amount I learned by just sitting with my mentor watching him churn through Vim, explain Vault and secrets managers, or blast through my code
with PyLint was invaluable. Thus, don't feel bad when your code looks like shit or lots of things can be optimized and changed.
At an internship, you're getting paid to learn. If you fuck up or can't figure out a problem, reach out to mentors and teammates to figure 
out the solution isntead of churning endlessly on a problem you can't figure out. No reason to ever get worked up over something like that.

**Second project:**

After learning Flask, my job became A LOT easier. My next project allowed custom routing within Mattermost for specific string searches.
If a developer wanted the output of a Jenkins build (where all jobs were posted to a #Jenkins channel), they could add a regex query to search 
output of Jenkins jobs and then route it through a direct message or specific channel. 

<hr>

#### Implementing DevOps

You'll notice that my two major projects this summer utilized Python and Flask. Not Ansible, Terraform, Docker, Jenkins (well, kind of), or 
many other commonly associated DevOps tools. 

Despite this, I consider this a successful internship and actually "implementing" DevOps. 

Our BRE team thought of an area where there was a gap between development and Ops 
(BRE in this case, so not specifically Ops), developed internal tooling to provide increased visibility between teams for specific builds,
and created a solution that bridged this gap.

<hr>

And that's it! Hope you enjoyed a brief rundown of my internship. Next blog I'm going to do a write up and tutorial on either Docker/TravisCI
or only Docker. Virtualization is suuuuuper interesting to me, so I hope you'll enjoy it too!

:peace:



