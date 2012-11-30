---
layout: post
title: "Drawing robots roundup"
date: 2012-01-15 09:58
comments: true
tags:
- drawing
- robot
- plotter 
- arduino
- processing
- graphics
- image processing
- painting
- plotter
- electronics
---
I intend to build a drawing robot soon as a part of a bigger project that will hopefully culminate in a short animation. I have just been given a broken HP Deskjet D4260 so I already have a few parts I might need. I am not yet fully decided on which approach to take, so here's a roundup of different drawing machines to inspire me. 

### Der Kritzler

<iframe src="http://player.vimeo.com/video/28003302?title=0&amp;byline=0&amp;portrait=0" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

Have I mentioned yet how much I love [Alex Weber's projects][1]? The one that led me to find his blog was [Der Kritzler][2] - a robot that draws on the windows. It uses a combination of [Processing][3], [ImageMagick][4] and [Potrace][5] to create the graphics and the movement of the bot itself is controlled by an Arduino. The device is suspended on notched tape which controls the movements.

### Hektor

<iframe src="http://player.vimeo.com/video/15823044?title=0&amp;byline=0&amp;portrait=0" width="500" height="375" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

[Hektor][6] was the project that made me fall in love with physical hacking, it's the first one of its kind that I could find - built in 2002. It's a small portable spraypainting device that can cover a huge wall area, but packs away into a small suitcase. Its construction directly inspired Der Kritzler - the spraycan's movements are controlled by toothed belts.

### Delta Robot

<iframe src="http://player.vimeo.com/video/25924581?title=0&amp;byline=0&amp;portrait=0" width="500" height="375" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

Arduino-controlled suspended plotter. 3 arms are controlled by servos. I like this one a lot despite the lack of precision. Its creator, [Puiu Bogdan][7], [explains][8] that the concept itself results in very precise drawings, but his implementation still needs to be perfected. Since it took him 7 months to build this prototype I reckon it's a little too complicated for my purposes. 

### 3-Axis servo motor

<iframe width="500" height="339" src="http://www.youtube.com/embed/v9x7Qdpp43M" frameborder="0" allowfullscreen></iframe>

Definitely can't make anything similar as I intend to use mine at home, but [this is cool][9]. 

### Senseless Drawing Robot

<iframe src="http://player.vimeo.com/video/30780208?title=0&amp;byline=0&amp;portrait=0" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

[This bot][12] built by [So Kanno][10] and [Takahiro Yamaguchi][11] uses a double-pendulum to randomise its graphic output. Pretty awesome.

### Polargraph

<iframe src="http://player.vimeo.com/video/24647023?title=0&amp;byline=0&amp;portrait=0" width="500" height="375" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
<iframe width="500" height="339" src="http://www.youtube.com/embed/UT8p1kLz8PI" frameborder="0" allowfullscreen></iframe>

[Euphyscott][13] made this [polargraph][14]. Although it's very slow in drawing these types of images, the end result is pretty neat. Also, bonus points for posting the code and detailed process descriptions on the [polargraph's website][14] and on [Instructables][16]. You can also [buy some of the bits used][15] to build your own from Euphyscott.

### Interactive Robotic Painting Machine

<iframe src="http://player.vimeo.com/video/23998286" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

[Benjamin Grosser][17]'s [creation][18] listens to its surroundings and the sound input affects the decisions the AI makes in its painting process. 

### Robo-rainbow

<iframe src="http://player.vimeo.com/video/19374769?title=0&amp;byline=0&amp;portrait=0" width="500" height="281" frameborder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>

[Akay][19]'s robo-rainbow was featured in [Wired][20] last year:

> A small circuit board featuring radio-controlled servos from a toy car drives the solenoids attached to each spray can, which in turn apply pressure to the nozzles. Both the arm and the spray cans are controlled using toy car's radio controller, allowing the user to move the arm in a smooth arc while spraying with each of the six spray cans simultaneously, creating a large rainbow painting within seconds.

### Pen plotter

<object type="application/x-shockwave-flash" width="500" height="375" data="http://www.flickr.com/apps/video/stewart.swf?v=109786" classid="clsid:D27CDB6E-AE6D-11cf-96B8-444553540000"> <param name="flashvars" value="intl_lang=en-us&photo_secret=3d4e830459&photo_id=6295455826"></param> <param name="movie" value="http://www.flickr.com/apps/video/stewart.swf?v=109786"></param> <param name="bgcolor" value="#000000"></param> <param name="allowFullScreen" value="true"></param><embed type="application/x-shockwave-flash" src="http://www.flickr.com/apps/video/stewart.swf?v=109786" bgcolor="#000000" allowfullscreen="true" flashvars="intl_lang=en-us&photo_secret=3d4e830459&photo_id=6295455826" height="375" width="500"></embed></object>

![Pen plotter image](http://farm7.staticflickr.com/6218/6294759696_7ed5be13f1.jpg)

And last but not least, my favourite, built by [Berticus][22]. This [pen plotter][23] traces input from the webcam to create some really awesome [portraits][21]. Just look at them! 

[1]: http://tinkerlog.com/
[2]: http://tinkerlog.com/2011/09/02/der-kritzler/
[3]: http://www.processing.org/
[4]: http://www.imagemagick.org/script/index.php
[5]: http://potrace.sourceforge.net/
[6]: http://hektor.ch/
[7]: https://plus.google.com/117437757896877369617
[8]: http://arduino.cc/forum/index.php/topic,65561.0.html
[9]: http://www.embeddedtronics.com/uhuservo.html
[10]: http://kannoso.org/
[11]: http://yang02.org/
[12]: http://thisisnotagraffiti.tumblr.com/
[13]: http://www.youtube.com/user/euphyscott
[14]: http://www.polargraph.co.uk/
[15]: http://www.polargraph.co.uk/build-or-buy-a-machine/
[16]: http://www.instructables.com/id/Polargraph-Drawing-Machine/
[17]: http://bengrosser.com/
[18]: http://bengrosser.com/projects/interactive-robotic-painting-machine/
[19]: http://www.akayism.org/
[20]: http://www.wired.co.uk/news/archive/2011-02/02/robo-rainbow
[21]: http://www.flickr.com/photos/bert_m_b/sets/72157628015314436/with/6294759696/
[22]: http://interlockroc.org/author/berticus/
[23]: http://interlockroc.org/2011/10/30/barcamp-rochester/
