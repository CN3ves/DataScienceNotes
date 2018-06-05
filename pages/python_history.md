[MUSIC] I worked at this place, CWI, and for my then current project, which was the Amoeba operating system, which I was working under Sape Mullender. One of our projects was to write application-level utilities for this new Amoeba operating system. And so, there was an operating system kernel and it was very good at talking to the network. And it was very good at managing processes. But there wasn't much user-level software. There was barely a shell, I think there was a ported, very old Unix shell something like the original Unix version six shell, but because the file system model on Amoeba was so very different we couldn't take an existing suite of Unix utilities. And so we wanted it to be self-hosting. And in order to that we realized we need a large amount of user-level sort of applications, utilities, tools, whatever you call it, from an editor to a mail program to a login utility and a backup tool. And one of the things I realized, as we had a small team of people sort of working on those things, that it was very slow going writing all that stuff in C, and it wasn't particularly interesting or sort of novel or difficult and often we also didn't really care how fast the code ran. All the reasons why you would write a piece of software in C didn't really apply. The only reason left was that C was the only language that for which we had a compiler. There was this ABC language that I had in the back of my mind that would be a much better language to write a whole bunch of utility application tools for Amoeba, except that ABC was so high and abstract that it really. It wasn't a good language to talk to servers and file systems and processes and it's sort of, the whole operating system thing was abstracted away from ABC. It was almost something like it, I don't know. In an alternate universe ABC could have become the language of spreadsheets. It was very good for talking about a user's data. And doing all sorts of clever stuff with that data. And it did that using very, sort of general all-purpose data structures like lists and dictionaries and of course it had very nice code structuring devices like a small number of simple statements that could be combined in any way you wanted to create other constructs. The usual function and procedure abstractions. It was not at all an object oriented language although the implementation had some objects sort of shining through. Anyway ABC as it existed still wasn't usable but I somehow, since I had worked on the ABC project, I knew exactly how it was built. And I had this idea in my head that, given how much time we had available for our project, I could actually build a whole new language, design and implement it from scratch, given what I learned about both the design and the implementation of ABC, and start using it to implement our suite of tools and still be ahead of the game compared to a situation where we would just have sort of clunked on writing the things we wanted to write in C. For three months, I did my day job and at night and whenever I got a chance I kept working on Python. I believe that within three months I was to the point where I could tell people, look here. This is what I built. And it had an interactive interpreter loop. So the first demos were all let's assign an expression to a variable and print it back. And let's define a small function and call it. And let's put some things in an array and iterate over the array. And all those things worked. And somehow, and I don't exactly know sort of how fast this happened, but certainly my two office mates were almost instantly taken with it and started helping out. And they and a few others within the institute were very excited about this thing that I'd built. And started sort of, of course we didn't instantly use it on Amoeba because it wasn't mature enough to actually write the Amoeba utilities that we wanted. But it was already instantly useful enough to run on our Unix system. People within CWI, even outside my own department, started using it. And recognizing that it was fun and productive to use. And they used it for small scripts and people started contributing things like bug fixes. Somehow things then went very quickly during that first year. Because I think by the end of 1990, so a year after I started, we developed a plan to do an open source release of this language. And this was before the word open source had even been coined. So we didn't call it that. But we did have some models. We had like X11, the window system at the time, had a distribution that was one of the sort of open source examples. With two colleagues I worked sort of building a distribution and we, actually it turned out to be very simple to get management to sign off on this release. That was an an incredibly lucky stroke. I just sort of, I asked my manager's manager what should we do about this and he said oh, you gotta talk to this and this person in the administrative branch of the institute. And I talked to this woman and she was like in charge of all legal affairs I believe and I said well I have written this source code and I would like to release that and I have sort of made up a license that's like identical to the MIT license, I could say MIT releases software under exactly this license and we just put like the formal name of our institute in there instead of the regents of the institute. She asked me some questions like did someone pay for this to be developed? And my answer was no, I started it all on my own time and it was for this research project and that sort of. My manager's fine with it. And so she said sure, go ahead. And we did it and that's so in February '91, we did the first Python release. It felt like, at the time like an incredible milestone. We needed to post it to Usenet. There was this Usenet newsgroup that would receive source code for random free projects. I got immediately started getting useful positive feedback from, well initially just from random people who picked up free software from Usenet. And we quickly sort of got into a routine of doing new Python releases. And every time, I mean there were the obvious improvements to the language and the library and bug fixes, a very important category of things that were often contributed were ports or ported fixes where people had different architectures, different compilers. The Unix world was much less homogenous at the time. There were lots of small Unix vendors that had their own compilers, or their own hardware. All sorts of things. So the big things that happened during say the first half of the '90s was a community of Python users and developers self-organized. Then came the invitation to come to the United States for a couple of months from NIST, the National Institute for Standards and Technology. So I spent two months there. We organized the first Python workshop, which was hosted by NIST. Through that Python workshop I met people who offered me a job and from '95, I mean I went back to the Netherlands for a few months and then from '95 to 2000 I worked in US in northern Virginia at CNRI. And so there we worked through a lot of growth of the community and the infrastructure. We created the Python website, I got in touch with a bunch of people who are still active in the Python community like Barry Warsaw. I think when I started there Python 1.3 was about to be released. And then while I was there we released several subsequent versions leading up to 1.5.2 which for some reason 1.5.0 was nothing but 1.5.2 remained the sort of the standard, the gold standard of Python for a very long time afterwards. [MUSIC]  [MUSIC] Python was created by Guido van Rossum in 1989 while working at CWI in the Netherlands. Python was released as Open Source in February. 1991. The open source community grew around the world. And the first Python workshop was hosted by NIST in 1994. >> From 95 to 2000, I worked in the U.S. in Northern Virginia at CNRI. And so, there we worked through a lot of growth of the community and the infrastructure. We created the Python website. I think when I started there, Python 1.3 was about to be released. And then while I was there, we released several subsequent versions leading up to 1.5.2. Which for some reason, 1.5.0 was nothing, but 1.5.2 remained the sort of, the standard, the gold standard of Python for a very long time afterwards. Disagreement was brewing between the people working on Python at CNRI and the CNRI leadership about open source. I was sort of courted by a small no name startup, and they said, oh, you gotta come work for us. We're an open source startup. We're going to build an open source portal. And find a number of other good Python engineers, and we'll give you all the time you want to sort of work on Python full time. And I thought, wow, that sounds great! Especially, given that I already had this sort of discontent at the place where I had been for five years, and so, reluctantly, I agreed to join these guys. Well, by then, by the time we actually started, it was 2000. And with, our start date was May 15, the bubble had actually already burst. I wasn't even aware that there was a bubble and that it had burst. I was in Northern Virginia doing open source software. I wasn't, I didn't really know what a startup was. I didn't really know how to tell whether these people were trustworthy or not. Well, we spent the summer in blissful ignorance working full time on Python. We built and released Python 2, which was a big deal. It contained Unicode. We also, because we had to have some kind of graceful exit from my previous employer, who claimed a certain amount of ownership over the source code. They didn't claim that it was all theirs, because it wasn't theirs to begin with. It was open source before I joined, which was an incredibly lucky circumstance. But, nevertheless, they sort of claimed ownership over what had been added to it over the five years I worked there and other people who were also employed there, also worked there. And so, with negotiations facilitated by Eric Raymond, and I think also even more in the background Eben Moglen, the free software lawyer, we negotiated some way to make sure that Python remained open source, with a license that CNRI's lawyers were agreeable to. And that was sort of, Python still has a very awkward license. And the history of that awkward license lies in the way I left CNRI. So, this little startup, we didn't even move to the west coast. We just sort of, we worked from our homes. And I remember that once a week, we had a team meeting and a catch-up with the leadership in California in my living room. And within five months, it was over. They suddenly stopped paying us. And those five months, we had had the time of our lives working on Python, doing this Python 2 release. We also had to do a Python 1.6 release, that was actually nearly identical to Python 2.0. That was the first Python 1.0 release with CNRI's license on it. And sort of over the summer and the fall of 2000, this startup company began to show more and more signs of dysfunction. Other teams suddenly disappeared. We later heard that they had been fired. They flew us out to the west coast to talk to random potential customers, to sort of show off our technical prowess and somehow, get some kind of deal where we would do work for a customer. None of those deals ever closed. So they were going deeper and deeper in the hole. And at the end of the year, the investors decided to stop funding it. And then suddenly, we were like, we were out in the streets. We were relatively well off, because we had been paid well until then. But, yeah, the company was gone. So, what, all we got out of it was, they had given each of us, they had bought each of us a good computer to work from home. So, that was our last payment. [LAUGH] Cuz we talked to lawyers or somehow we got advice where someone said, yeah, sure. Just hold onto that equipment. Nobody's going to have the power to take that away from you. They're not going to go after you. And so, then there was actually, well I wouldn't call it a bidding war. But we were negotiating with both Active State, which was a small software company in Vancouver, and Zope Corporation, which was a small Python-exclusive software company in Northern Virginia. And the whole Python labs team, five of us, ended up working for Zope. And that was an incredibly lucky rescue. >> With the terms and conditions that pretty much keep working on Python, right? I mean, that Zope didn't tell you you had to go- >> No, Zope was very clear. They said, we have no design on the ownership of that software. We want you guys, you guys are really good programmers. You guys are the top of the Python community. You are going to get some time and it wasn't stated very precisely how much time. And we were fine with that at the time. We realized that what we had done for this failing startup was not actually a realistic option. That they would just pay our salaries and we would only do open source development. Nobody could maintain that, so we had sort of grown up quickly. We did continue to do a lot of sort of fundamental Python work at the time at Zope. We also did a lot of fundamental Zope work. Over time, sort of, the team dispersed. I got a job offer to come work for a small startup again in California. This time I did my homework a little better. Python just kept, sort of, growing, and the community kept self-organizing. And so, what started out as a workshop we had with about 20, 25 people at most attending in '94. Within a few years, we had an annual, what we called the International Python Conference, with with three or four hundred people attending. I always encouraged the community to self-organize rather than sort of looking at me for every decision. And so, one of the things that gradually appeared was the notion of Python warts. I'm not sure, but I think that Andrew Kuchling was actually one of the first to talk about Python warts, and sort of blog about it or give a talk about it. Of course, different people have different ideas about what's wrong with Python. But, sort of the idea of warts is things that keep tripping people up over and over. And so, there is at least some notion of, these are objectively problems. Every sort of feature release, 2.1, 2.2, 2.3. We tried to fix some of these things. But we also came up against a wall of things that we could never fix because the fix was sort of, required changing the language in an incompatible way. Because it's always easy to add new syntax, that sort of doesn't get in the way of existing syntax. But it's very hard to take away a particular syntactic construct that has an unfortunate but well-defined meaning. And all these things built up and, sort of, in the middle of the first decade of the new century, this idea of Python 3000 was born. Like, okay, we have so many things that we would like to fix. We know roughly how to fix them, but the fix would be incompatible. Let's create a new version of the language that fixes a whole bunch of those things together. While at the same time, not making the new version of the language so different that it alienates the users. Every year at PyCon, I sort of take the census of well, who is using Python 3 and how committed are they? And how happy are they? And sort of, are there users actually using Python 3? And, I see tremendous progress there every year. But, we're still not, we're not in, sort of, where we finally want to be. I mean, at the last PyCon conference, I had to, sort of, hold off a whole bunch of people with very good arguments of why we should do a Python 2.8 release. And so, Python 3 is winning the race. But it will, the race hasn't been run yet. We're still in the race. It's clear that Python 3 is going to win it. [MUSIC]