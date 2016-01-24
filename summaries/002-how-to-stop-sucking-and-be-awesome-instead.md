How to Stop Sucking and Be Awesome Instead
==========


Jeff Atwood, March 2013, 247 pages

[Amazon](http://www.amazon.com/How-Stop-Sucking-Awesome-Instead-ebook/dp/B00BU3KPQU)

[Goodreads](https://www.goodreads.com/book/show/17670898-how-to-stop-sucking-and-be-awesome-instead)

About the author
----------------

Jeff Atwood is the author of [Coding Horror](http://blog.codinghorror.com/) and the co-founder of the [Stack Overflow](http://stackoverflow.com) the best programming Q&A forum and a part of greater Q&A [Stack Exchange](http://stackexchange.com/) network. He's been programming for a living since the 80ies. 

Introduction
============

The book is a compilation of the best posts from the Coding Horror blog, and got my attention from several recommendations for developers I ran into. I've also read several blog posts there and was happy to get a book with the most popular posts in a book form. 

As the book is a compilation of blog posts, it's a collection of essays, organized in several sections (How to suck less, Programming, Web Design Principles, Testing, Know your user, Causes we should care about, Gaming and Things to read) which contain the chapters, organized by the common theme.

Summary
=======

I. How To Suck Less
----------------
Section starts with Author's annoyance about the TODO lists, where he says that the proliferation of TODO tools is masking the fact that for the most important things in life he never needed a TODO list.

>If you can't wake up every day and, using your 100 percent original equipment, God-given organic brain, come up with the three most important things you need to do that day—then you should seriously work on fixing that. I don't mean install another app, or read more productivity blogs and books. You have to figure out what's important to you and what motivates you; ask yourself why that stuff isn't gnawing at you enough to make you get it done. Fix that. <br>Tools will come and go, but your brain and your gut will be here with you for the rest of your life. Learn to trust them.

The goof off time is important, and it wasn't invented by Google, apparently HP was the first known company to have a certain time off for their employees to play, invent and innovate. However, it only works if there's some slack in the schedule, if daydreaming and experimentation are allowed.

The chapter on persuasion shows clearly that to be able to effectively achieve something, persuading others is more valuable than commanding them:

>I was recently asked how I run our development team. I said, ‘Well, basically I blog about something I think we should do, and if the blog post convinces the developers, they do it. If not, I lobby for it, and if that fails too, the idea falls on the floor. They need my approval to launch something, but that’s it. That’s as much ‘running things’ as I do, and most of the ideas come from other people at this point, not from me and my blog posts. I’ve argued against some of our most successful ideas, so it’s a good thing I don’t try to exert more control.

In the story about [Microsoft Bob](https://en.wikipedia.org/wiki/Microsoft_Bob) we see how a failure can be a wonderful teacher.

>Failure is a wonderful teacher. But there's no need to seek out failure. It will find you. Whatever project you're working on, consider it an opportunity to learn and practice your craft. It's worth doing because, well, it's worth doing. The journey of the project should be its own reward, regardless of whatever happens to lie at the end of that journey. The only truly failed project is the
one where you didn't learn anything along the way.

Being distrustful of expertise, our own and others' is the right way to go, because being an expert means asking the right questions, not telling others what to do.

>Being an expert isn't telling other people what you know. It's understanding what questions to ask, and flexibly applying your knowledge to the specific situation at hand. Being an expert means providing sensible, highly contextual direction.

The dangers of being 90% done are in not writing things down - how to you know how much there's left to do if there's not a detailed list of things that need to be done?

**Boyd's Law of Iteration: speed of iteration beats quality of iteration.** 

* Unit tests should be small and fast, so you can run them with every build.
* Usability tests work best if you make small changes every two weeks and quickly discard what isn't working.
* Most agile approaches recommend iterations no longer than 4 weeks.
* Software testing is about failing early and often.
* Functional specifications are best when they're concise and evolving. 

The part about overnight success which takes years was pretty comforting, and it referenced the unavoidable [Teach Yourself Programming in Ten Years](http://www.norvig.com/21-days.html) essay. Any significant success needs years of dedicated effort. 

II. Programming
-----------

The section about programming has a number of insights and advice to programmers looking to get better. The first one is a bit paradoxical: How to become a better programmer by not programming? The answer is to become passionate about your users, about your business.

>To truly become a better programmer, you have to to cultivate passion for everything else that goes on around the programming.


It moves on to the broken window theory, where the lesson is that having "broken windows" in the code (disfunctional code, entire sections commented out, etc) breeds more code rot. 

>Programming is insanely detail oriented, and perhaps this is why: if you're not on top of the details, the perception is that things are out of control, and it's only a matter of time before your project spins out of control. Maybe we should be sweating the small stuff.

The lessons from development of the Forth programming language illustrate the timelessness of the computer wisdom:

1. **Keep it simple:** As the number of capabilities you add to a program increases, the complexity of the program increases exponentially. The problem of maintaining compatibility among these capabilities, to say nothing of some sort of internal consistency in the program, can easily get out of hand. You can avoid this if you apply the Basic Principle. You may be acquainted with an operating system that ignored the Basic Principle. It is very hard to apply. All the pressures, internal and external, conspire to add features to your program. After all, it only takes a half-dozen instructions, so why not? The only opposing pressure is the Basic Principle, and if you ignore it, there is no opposing pressure. 
2. **Do not speculate:** Do not put code in your program that might be used. Do not leave hooks on which you can hang extensions. The things you might want to do are infinite; that means that each has 0 probability of realization. If you need an extension later, you can code it later—and probably do a better job than if you did it now. And if someone else adds the extension, will he notice the hooks you left? Will you document this aspect of your program? 
3. **Do it yourself:** The conventional approach, enforced to a greater or lesser extent, is that you shall use a standard subroutine. I say that you should write your own subroutines. Before you can write your own subroutines, you have to know how. This means, to be practical, that you have written it before; which makes it difficult to get started. But give it a try. After writing the same subroutine a dozen times on as many computers and languages, you'll be pretty good at it.

A good way of keeping uncertainty to a minimum and maintaining clarity in the code is merciless deleting of anything not used:

>If you have a chunk of code you don't need any more, there's one big reason to delete it for real rather than leaving it in a disabled state: to reduce noise and uncertainty. Some of the worst enemies a developer has are noise or uncertainty in his code, because they prevent him from working with it effectively in the future.<br><br>A chunk of code in a disabled state just causes uncertainty. It puts questions in other developers' minds: <br><br>• Why did the code used to be this way? <br><br>• Why is this new way better?<br><br>• Are we going to switch back to the old way?<br><br>•How will we decide?<br><br>If the answer to one of these questions is important for people to know, then write a comment spelling it out. Don't leave your co-workers guessing.

An emphasis on the code quality today should be very important, and pointed out through the following:

1. Do you use source control? 
2. Can you make a build in one step? 
3. Do you make daily builds? 
4. Do you have a bug database? 
5. Do you fix bugs before writing new code? 
6. Do you have an up-to-date schedule? 
7. Do you have a spec? 
8. Do programmers have quiet working conditions? 
9. Do you use the best tools money can buy? 
10. Do you have testers? 
11. Do new candidates write code during their interview? 
12. Do you do hallway usability testing?

The ways to practice our craft are not just by writing code

1. Write your resume. List all your relevant skills, then note the ones that will still be needed in 100 years. Give yourself a 1-10 rating in each skill. 
2. Make a list of programmers who you admire. Try to include some you work with, since you'll be borrowing them for some drills. Make one or two notes about things they seem to do well—things you wish you were better at. 
3. Go to Wikipedia's entry for ["Prominent pioneers in computer science"](https://en.wikipedia.org/wiki/List_of_pioneers_in_computer_science) section, pick a person from the list, and read about them. Follow any links from there that you think look interesting. 
4. Read through someone else's code for 20 minutes. For this drill, alternate between reading great code and reading bad code; they're both instructive. If you're not sure of the difference, ask a programmer you respect to show you examples of each. Show the code you read to someone else, and see what they think of it. 
5. Make a list of your 10 favorite programming tools: the ones you feel you use the most, the ones you almost couldn't live without. Spend an hour reading the docs for one of the tools in your list, chosen at random. In that hour, try learn some new feature of the tool that you weren't aware of, or figure out some new way to use the tool. 
6. Pick something you're good at that has nothing to do with programming. Think about how the professionals or great masters of that discipline do their practice. What can you learn from them that you can apply to programming? 
7. Get a pile of resumes and a group of reviewers together in a room for an hour. Make sure each resume is looked at by at least three reviewers, who write their initials and a score (1-3). Discuss any resumes that had a wide discrepancy in scoring. 
8. Listen in on a [technical phone screen](http://www.codinghorror.com/blog/archives/001042.html). Write up your feedback afterwards, cast your vote, and then talk about the screen with the screener to see if you both reached the same conclusions. 
9. Conduct a technical interview with a candidate who's an expert in some field you don't know much about. Ask them to explain it to you from the ground up, assuming no prior knowledge of that field. Try hard to follow what they're saying, and ask questions as necessary. 
10. Get yourself invited to someone else's technical interview. Listen and learn. Try to solve the interview questions in your head while the candidate works on them. 
11. Find a buddy for trading practice questions. Ask each other programming questions, alternating weeks. Spend 10 or 15 minutes working on the problem, and 10 or 15 minutes discussing it (finished or not.) 
12. When you hear any interview coding question that you haven't solved yourself, go back to your desk and mail the question to yourself as a reminder. Solve it sometime that week, using your favorite programming language.

 
Working alone as a developer is a special kind of hell, there is nobody to bounce ideas off, nobody to review your code, and code review is very important:

>In a healthy software engineering culture, team members engage their peers to improve the quality of their work and increase their productivity. They understand that the time they spend looking at a colleague's work product is repaid when other team members examine their own deliverables. The best software engineers I have known actively sought out reviewers. Indeed, the input from many reviewers over their careers was part of what made these developers the best. 

III. Web Design Principles
---------------------

What makes a great front page for a web application?

1. Loads reasonably fast
2. An elevator pitch on the first page
3. Show an example, because [ideas are worthless and execution is everything](http://blog.codinghorror.com/cultivate-teams-not-ideas/)
4. Give a clear, barrier free call-to-action
5. Embrace your audience even if it means excluding other audiences. Don't patronize your potential users by telling them everybody should care about _insert your app here_.

We should always be in the pursuit of simplicity, no matter what it takes. **Features don't matter**:

>These people don't care about your flexible, brilliant architecture. They don't wish to tweak settings. They don't want to spend more than 10 consecutive seconds confused. They just want simple, they want to get their task done and move on. They don't want to spend time learning anything because they know they'll probably just forget it long before they'll need to do it again anyway.
 
 
With the rise of mobile apps, it becomes clear that in a lot of cases they are winning over websites. The lesson to take here is 

>Design simple things that scale up; not complicated things you need to scale down (for mobile).

When it comes to coding, **favor consistency over cleverness**.

>Because you won't be the only person to work on this code. Even if you are, the next time you touch it might be a year or two from now. If you did something clever, the next person to touch it will look at the code and not immediately understand. This will have one of two consequences. Either they will have to spend 10 minutes just trying to understand what it is you did or, worse, they will assume you made a mistake and ‘fix’ it by making it less clever. Neither of these results is desirable.

When experimenting with UI, you **must have a good reason** to deviate from the convention:

1. Have a complete understanding of the current convention and how it arose
2. Have a good, reasoned argument for deviating from the convention 
3. Collect usage data on your experiments 
4. Make decisions based on the usage data

>If you're not collecting usage data, or your reason is "it looks better this way," then you're doing it wrong, and you should stick with the conventions.

Usability testing is **one of the best ways people can improve their websites**. The recommended book is [Rocket Surgery Made Easy](http://www.amazon.com/dp/0321657292/)

Section continues to discuss the difference between _usability_ and _learnability_.

>It takes several weeks to learn how to drive a car. For the first few hours behind the wheel, the average teenager will swerve around like crazy. They will pitch, weave, lurch, and sway. If the car has a stick shift they will stall the engine in the middle of busy intersections in a truly terrifying fashion.<br><br>If you did a usability test of cars, you would be forced to conclude that they are simply unusable.<br><br>This is a crucial distinction. When you sit somebody down in a typical usability test, you're really testing how learnable your interface is, not how usable it is. Learnability is important, but it's not everything. Learnable user interfaces may be extremely cumbersome to experienced users. If you make people walk through a fifteen-step wizard to print, people will be pleased the first time, less pleased the second time, and downright ornery by the fifth time they go through your rigamarole.<br><br>Sometimes all you care about is learnability: for example, if you expect to have only occasional users. An information kiosk at a tourist attraction is a good example; almost everybody who uses your interface will use it exactly once, so learnability is much more important than usability. But if you're creating a word processor for professional writers, well, now usability is more important.<br><br>And that's why, when you press the brakes on your car, you don't get a little dialog popping up that says ‘Stop now? (yes/no).’”

With the story about launching iTunes and label people pitching ideas to Steve Jobs, we are told that
>Innovation is not about saying yes to everything. It's about saying NO to all but the most crucial features.

For most programmers, UI is hard, so that's why we should start with the UI first. We tend to think in code and features instead of how to make it easier for the users.

IV. Testing
-------

The true value of running unit tests is that it makes us _think_ about testing. Like, what are the most common use cases, what are the probable unusual cases, and what should be tested.

The author is stacked against unit testing when beta testing is an option. And that is because programmers tend to _test safely_. 

>Real testers hate your code. A unit test simply verifies that something works. This makes it far, far too easy on the code. Real testers hate your code and will do whatever it takes to break it—feed it garbage, send absurdly large inputs, enter unicode values, double-click every button in your app, etcetera.


And

>Users are crazy. Automated test suites are a poor substitute for real world beta testing by actual beta testers. Users are erratic. Users have favorite code paths. Users have weird software installed on their PCs. Users are crazy, period. Machines are far too rational to test like users.

If our users are telling us more about existing bugs then we know, then we're failing at our job which is to **know more about our application's health then users do**. He also makes a good point in saying that our exception logs are a de-facto to-do list for the development team. He calls that **exception driven development**.

If we fix a bug that no user will ever encounter, what have we actually fixed?

>Ship your software, get as many users in front of it as possible, and intently study the error logs they generate. Use those exception logs to hone in on and focus on the problem areas of your code. Rearchitect and refactor your code so the top 3 errors can't happen any more. Iterate rapidly, deploy, and repeat the process. This data-driven feedback loop is so powerful you'll have (at least from the users' perspective) a rock stable app in a handful of iterations.

V. Know your user
--------------

Here, we're reminded that possibly the greatest sin software developers commit is **consider themselves the average user**. Nothing could be farther from the truth. The average user doesn't know _what ALT+TAB does_.

Referencing the [Inmates Are Running The Asylum](http://www.amazon.com/exec/obidos/ASIN/0672316498) we are shown how most software is actually designed by sotware developers, ie. _Homo Logicus_ where our users are plain old _Homo Sapiens_

>For Homo logicus, control is their goal and complexity is the price they will pay for it. For normal humans, simplicity is their goal, and relinquishing control is the price they will pay. In software-based products, control translates into features. For example, in Windows 95, the "Find File" function gives me lots of control over the procedure. I can specify which area of my disk to search, the type of file to search for, whether to search by file name or by file contents, and several other parameters. From a programmer's point of view, this is very cool. For some extra up-front effort and understanding, he gets to make the search faster and more efficient.<br><br>Conversely, the user's point of view is less rosy because he has to specify the area of the search, the type of file to search for, and whether to search by name or contents. Homo sapiens would gladly sacrifice the odd extra minute of compute time if they didn't have to know how the search function works. To them, each search parameter is just another opportunity to enter something incorrectly. The probability of making a mistake and the search function failing is higher, not lower, with the added flexibility. They would gladly sacrifice all that unnecessary complexity, control, and understanding in order to make their job simpler.

The disappointing fact in the software industry is that most developers have no contact with their users. They never see how people actually use their product.
 
Another great point is that _shipping isn't enough_.

>Programming is fun. It is the joy of discovery. It is the joy of creation. It is the joy of accomplishment. It is the joy of learning. It is fun to see your handiwork displaying on the screen. It is fun to have your co-workers marvel at your code. It is fun to have people use your work. It is fun have your product lauded in public, used by neighbors, and discussed in the press. Programming should be fun and if it isn't, figure out what is making it not fun and fix it. However, shipping isn't fun. I often have said that shipping a product feels good, like when someone stops hitting you. Your job is completing the product, fixing the bugs, and shipping. If bugs need fixing, fix them. If documentation needs writing, write it. If code needs testing, test it. All of this is part of shipping. **You don't get paid to program, you get paid to ship**. Be good at your job.

The ultimate metric of success is **how many real users actually use our product**.

Users also lie. Not because they are bad people, but because they, as everyone else, lack objective self awareness:

>But like all of us humans, they're unreliable at best. **In order to move beyond usability guesswork, there's no substitute for observing customers using your product**. Wouldn't it be liberating to be able to make design decisions based on the way your customers actually use your software, rather than the way they tell you they use it? Or the way you think they use it? Whether you're observing users in low-fi usability tests, or collecting user action data so you can observe users virtually, the goal is the same: **don't ask—observe**.

VI. Cases We Should Care About
------------------------------

This part of the book discusses Net Neutrality, Copyright and preserving the Internet as a part of the Internet Archive.

VII. Gaming
-----------

Here, the author reminisces how programming do-it-yourself games got a lot of developers into programming in the first place.

VIII. Things To Read
--------------------

It's a shocking discovery to find out most programmers don't read books.
Some of the reasons why are:

1. Most programming books suck
2. Programming books are sold by weight, not by volume
3. Quick-fix books oriented towards novices

If you read one programming book per year, pat yourself on the back, because that's more than most programmers do. The five programming books every working programmer should own and read are:

1. [Code Complete 2](http://www.amazon.com/exec/obidos/ASIN/0735619670)
2. [Don't Make Me Think](http://www.amazon.com/exec/obidos/ASIN/0321344758)
3. [Peopleware](http://www.amazon.com/exec/obidos/ASIN/0932633439)
4. [Pragmatic Programmer](http://www.amazon.com/exec/obidos/ASIN/0932633439)
5. [Facts And Fallacies](http://www.amazon.com/exec/obidos/ASIN/0321117425)

Other books recommended by the author are

* [59 Seconds: Think a Little, Change a Lot](http://www.amazon.com/59-Seconds-Little-Change-Borzoi/dp/B0057DCE7M/) the only self-help book the author believes is worth your money - because it's based entirely on scientific knowledge, and not feel-good mumbo-jumbo
* [The Cuckoo's Egg: Tracking a Spy Through the Maze of Computer Espionage](http://www.amazon.com/dp/1416507787/) is a book about first case of malicious hacking, back in 1986
* [Ghost in the Wires: My Adventures as the World's Most Wanted Hacker](http://www.amazon.com/dp/0316037702/), an autobiographical book about Kevin Mitnick, the first high-profile computer hacker
* [Kingpin: How One Hacker Took Over the Billion-Dollar Cybercrime Underground](http://www.amazon.com/dp/0307588688/) is about post year 2000 computer crime
* [How to Talk So Kids Will Listen & Listen So Kids Will Talk](http://www.amazon.com/dp/0380811960/) is more than a book about communicating with kids, it's applicable to every human you encounter, full of insights on human interaction
* [The New Turing Omnibus: Sixty-Six Excursions in Computer Science](http://www.amazon.com/exec/obidos/ASIN/0805071660), a grab-bag of computing topics; Each chapter is the equivalent of a short blog post examining a particular topic, peppered with tables, diagrams, and illustrations.


Conclusion
==========

While the book was mostly a enjoyable and enlightening read, some of the posts felt more like rants than informative essays. Fortunately, there were only a few and the remainder of the material was a no-nonsense wisdom of an industry veteran. 

The relaxed, conversational writing style was refreshing and kept my attention very well. I would recommend the book to the novice and experienced developer alike. 