---
layout: post
title: "Why Not - PHP Frameworks"
date: 2014-12-03 17:35:14 +0000
comments: true
categories:
- Why
- PHP
- Frameworks
---
I’m writing this after more than two years since we took the decision to do the core development of our apps using plain *PHP* and to tell you the truth ditching object oriented programming as well.
<!--more-->
I know that the current core is based on [Phalcon](http://www.phalconphp.com/) and it work pretty well for what I’ve been told; probably using a resonable framework is the way to go, just please bear with me to understand the reasoning and the decision behind the choice of going with pure *PHP*.

First thing let me tell you that when the development started we were already late (nothing new, you could say). Since I wasn’t experienced with any framework I decided to go with plain *PHP*. At the end of the day *PHP* already provided most of the functionalities I needed. *Object Oriented Programming* was discarded as the website was pretty straightforward:

* A few static pages
* A login page
* A *place a bet* page
* A user area
* A result page

To implement this the structure of the application was made of: 

* A routing function (a simple switch statement) 
* Several support libraries where the business logic and database accesses were implemented. 

In less than a week we had the prototype ready to roll allowing us to secure the project.

The structure of the libraries was created following the *Unix philosophy*: each library would implement a small set of independent functionalities and structured so that each function could be either invoked by *PHP* directly or used as web services with a simple wrapper. 
In this way we could distribute the application on several servers splitting logically the functions. This was working fairly fine and allowed us to create some Flash applications using the web services created with no effort.

Then the revolution came, we had a team and and it was decided to go mainstream. We wrote everything from scratch using *Symfony 2* and *Doctrine*: it took us two weeks non stop but the result was evidently better. I learnt many new things: bundles, ORM, Composer, injections…it was an exciting experience.

Now if you ask me if I would use *Doctrine*, I’d be having mixed feelings. On *Symfony2*, I’d be prone to say no. But this is my personal opinion.

The person that took my place rewrote everything again using *Phalcon*, I’ve not used it so I cannot say anything.

Back to the original question: would I use an existing PHP framework for a development? Not so sure…now I’m able to design a good and flexible routing engine with small effort. Security (sql injections, overflows…) is pretty well implemented with the basic PHP functions. Probably I’d push all the audit functions to the DBMS using triggers. Where I really enjoyed the advantages of the forms. But beside that…I’d rather create an ad hoc framework fit for the needs.

I understand that there’s no need to reinvent the wheel and I completely support that philosophy but the building blocks for PHP are big and complex enough to allow an average web development to be lead without the need of a framework.

Unfortunately, or for better, I left the PHP world and I stopped devloping and investigating other frameworks.

Anyone for any good suggestion?
