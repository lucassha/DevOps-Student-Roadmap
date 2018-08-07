### August 2018 - Blog1
#### Phoenix Project: Understanding the why before the how

Hi everyone, welcome to my second blog post about a DevOps journey, 
where I’ll be talking about why reading the Phoenix Project is important and rambling about a few concepts within it afterwards. 
Bear with me on this one, as it is pretty much entirely conceptual. 

<hr>

#### So, what is the [Phoenix Project](https://www.amazon.com/Phoenix-Project-DevOps-Helping-Business/dp/0988262592) and why read it?

##### WHAT:

Basically, it’s the story of a guy being thrown into the fire of a lethargic, failing company that has not yet realized the importance of integrating IT within its larger business model. 
It is seen as a hindrance and area to potentially be outsourced instead of an area that provides a competitive advantage to the company. 
Like most good stories, this book is predominantly about the journey of putting out endless fires while getting burned on numerous occasions 
instead of the actual enlightenment of having achieved “DevOps.” 
Note, that last little bit was tongue-in-cheek.

##### WHY: 

If you are reading this blog, then I am assumign this is your first foray into the field (myself included, of course).
As such, Phoenix Project allows you to conceptualize and internalize many of the components of DevOps that would otherwise be abstract.
How do ops people communicate with developers? What role does security play in ops? How should IT communicate with upper management?
All of these things are answers from ten thousand feet as we follow Bill, the newly promoted VP of IT Ops, through his journey.

Without context on why you are doing something, implementing DevOps is just mashing a bunch of open source tools together and adding as many 
buzzwords as you can find along the way. This book's end goal is not to give a solution for your problems but enable you to think strategically
about what role IT Operations plays in an organization and the ability to find pain points to improve upon.

<hr>

#### Concepts

The entire book is driven from the principle of the "Three Ways," which you can read about from the author, 
Gene Kim, [here](https://itrevolution.com/the-three-ways-principles-underpinning-devops/).
These principles take many components of LEAN manufacturing and IT-morphize it into similar principles for IT.

It breaks down to this:
1) Systems thinking
2) Continual, consistent feedback loops
3) Create a culture of continuous experimentation and learning

Because I'm not going to do a better job explaining these concepts than the author himself, I'd encourage everyone to read this article as well.
He does a great job summing up the book's core principles in a few hundred words.

#### A few thoughts

Coming from a manufacturing and supply chain background before going back to school for CS,
one component of this book really stuck out to me: **unplanned work**.
In manufacturing, this is equivalent to WIP (work in process or progress, whichever floats your boat).
In a plant, WIP can mean a couple different things:

* Resources are tied up. You can think of it like a traffic jam. Once one lane starts getting clogged, 
multiple other lanes are affected as well. This is what you would term a **bottleneck**

* Product is not getting out the door. Your inventory and raw materials are not getting converted into revenue. 
As more WIP sits on the plant floor, both your resources and dollars are tied up 

How does this port over to IT?

* Resources can be tied up in a similar manner. In this case, it may be a specific person with more domain knowledge about a platform than others.
If there's unplanned work in that area, they will be the sole bottleneck and WIP will be created.

* In many cases, a physical product is not getting shipped out the door within IT. The equivalent could be a new feature or upgrade.
If these releases are being pushed back due to unplanned work and firefighting, that means it's the WIP sitting on the factory floor.

In the book, a specific resource, Brent, is in many cases the bottleneck to progress within the business. 
The company is consistently firefighting unplanned work, such as a payroll system going down. When this happens, Brent is drawn away from the Phoenix Project, 
which is the company’s forward-looking project that will level the playing field with their competitors.

When thinking about the first principle, here are a couple things to consider:

1) Profound understanding of the system is not being implemented. 
A single SME is solving this problem without anyone else understanding the root cause of the issue

2) This unplanned work is creating technical debt and setting back the rollout of their new features that will modernize the company


Phoenix Project does an excellent job at driving home how to think critically about the business and IT’s role within it. 
You won’t learn about a single tool in this book, and that’s really the point of it. 
Think about the purpose of DevOps and not just the fat salary that sometimes comes along with it.  

<hr>

#### A smaller sample

If you're looking for something a little shorter, [take a look at this article](https://itrevolution.com/devops-at-nike/), from the same site Gene posted on
about Nike trying to modernize and enable a forward-thinking engineering culture within their organization.
I wouldn't take this as gospel, but it's a pretty good example.

As the guy states:

```
…it’s not about technology, it’s not about the tools, it’s not even so much about the process. It’s more about this cultural accountability for the work that you do.
```

<hr>

#### Still there?

Hope you're still with me! I could easily write about Phoenix Project and its background in manufacturing for hours, so I hope this **VERY**
brief summation was at least a little helpful and not dreadfully boring. As this repo has gained a bit of traction, I'd love to hear from others and their experience
in these areas. Feel free to add your own info and thoughts into the blog post with a commit or PR.

<hr>

#### Next up

This summer, I worked as a Build and Release Engineer Intern in Portland, so I'm planning on writing about that experience.
What it was like interviewing, the work experience, areas I should have improved upon coming into the internship, and just anything within that realm.
Hopefully this time it takes me about 2 weeks to update instead of 4 months :| 

In the meantime, I added a bunch of [AWS notes](https://github.com/lucassha/AWS/tree/master/linux-acad-notes) that are useful for the CSA exam.
Feel free to fork them, but they are for the old exam instead of the new one. I am unsure how closely correlated they are.

Until next time!



