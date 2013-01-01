---
layout: post
title: "Notes from the coding workshop at Goldsmiths"
date: 2012-12-16 15:17
comments: true
tags: 
- goldsmiths
- teaching
- coding
- web
- programming
- workshop
---
On Friday I have finished [teaching coding][3] to [design][1] students at [Goldsmiths][2]. 

What I really wanted to teach was how to get data from various places on the web and how you can manipulate the data to make it become something else. I realised that the least amount of time spent on setting up would be if I did that by introducing JavaScript, since everyone has it available in the browser (by that I mean the students and not *actually* everyone). I would have loved showing them Ruby, but they were using their own computers I didn't want to risk a situation where I would spend an hour debugging someone's Ruby installation going awry and possibly putting them off ever trying programming after such an unfortunate start. Only a couple of students have had any programming experience: one of them played with Processing before, another with C.

To start with JavaScript I had to start with HTML. I am of the view that *everyone* should be able to read and write HTML, and so it seemed to make sense to go through HTML, CSS and JavaScript all together (some course notes and links are [all collected on the course site][3] on GitHub if you were interested in the structure of the course). I have seen people having to learn these basics (or at least the first two) in completely unrelated jobs, so hopefully these skills will come in handy even if the students don't all end up pursuing coding as a hobby or in their creative work.

![Visual Twitter](http://farm9.staticflickr.com/8499/8274548508_3460a02d10_z.jpg)
_Visual Twitter_

I've learnt loads by teaching, and all these things seem so *obvious* now.

### Teaching CSS is hard.

I have spent the first day explaining how the web works, and what is hypertext, and why all of this is worth knowing. I showed that browser is just a fancy way of viewing text files sent over the internet and how it will display your pages even if you litter them with mistakes. We then spent some time investigating various tags, editing code on existing websites and finally moved on to build a sample page or two in HTML before we dived into CSS. 

Then we got to CSS. I had tried to make it as simple as possible and only teach the basics, but there is no way of getting away from explaining inheritance, specificity, the box model and floats. The fact that the structure of the CSS document wasn't a one-to-one mapping of the underlying HTML structure was also confusing.

Very quickly I had to show some of them the [clearfix][4] hack, and I struggled to explain float clearing in a way that made sense. It also wasn't very reassuring when I explained that I start almost every project from including this workaround.

### JavaScript is easier than CSS.

Okay, maybe trolling *a little*. JavaScript is easier *to teach* than CSS. Especially when using jQuery.

I did what I now think of as group programming, which is a slightly expanded version of pair programming (I'm sure I haven't invented it and it's a popular way of teaching to program, but as I lack formal education in this regard I haven't come across anything like that before).

I was writing the code projected on the wall while explaining what I'm doing and why, and the students followed. The little project we were working on was slowly increasing in complexity, and I kept introducing new things as we needed them. As we progressed new questions were arising. This seemed to work very well and we managed to make two small projects on the first day. 

The next day we were working on visual Twitter: getting tweets via Twitter API and then fetching photos from Flickr matching the words in the tweet. By the end of the session one of the students said she could now read code and know what it did. I think they've become a lot more comfortable with JavaScript than they did with CSS.

### I took a wrong approach to teaching CSS.

My understanding of positioning, floats, box-model and the cascade stems from playing with CSS over the years. So I thought that the best way to grow to understand these things is to talk about them for a little bit and then to play with them. I have prepared a sample page with some CSS applied that forms a base for trying some of the things without having to write everything from scratch. I also encouraged students to write CSS for the page they made to solve some real problems and challenges. Turns out that perhaps this wasn't the best and least confusing way. 

 I think I could get much better results if I approached CSS in the way I did JavaScript and group-coded a sample project that would gradually increase in complexity. Building up confidence in using the language in that way is just as useful as building up the skill.

### A lot of things I take for granted about developing for the web don't make sense to a newcomer.

The separation between HTML, CSS and JavaScript, what they are used for and differences in syntax is something I don't think about until I have to explain them. To my students it was an odd thing to start with, as they are used to creating documents in a different way. I hope that by the end of the course it made sense why it's a good idea to separate content from presentation and how are markup and programming different. 

Some things made me a little bit embarrassed: the fact that we have to paper over browser inconsistencies with workarounds, that we have to provide fallback for audio and video, and that there aren't simpler ways of doing things like layout (well, not reliably across browsers yet). They seem like such simple, straightforward things.


![A random reason for needing a tutorial generator](http://farm9.staticflickr.com/8502/8274549572_b38ddeb9fe_z.jpg)
_A random reason for needing a tutorial generator_

The group I was working with was pretty much evenly split with regards to gender, which obviously made me very happy. It was a pleasure working with all of them. Once we finished, one of the students told me that before the course that he thought coding was hard; now he doesn't. I call that a success.


[2]: http://www.gold.ac.uk/design/
[1]: http://goldsmithsdesignblog.com/
[3]: http://ntlk.github.com/creative-coding-2012/
[4]: http://nicolasgallagher.com/micro-clearfix-hack/