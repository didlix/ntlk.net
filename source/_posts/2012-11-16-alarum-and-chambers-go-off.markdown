---
layout: post
title: "Alarum; and chambers go off"
date: 2012-11-16 08:31
comments: true
tags: 
- alarum
- rsc
- caper
- electronics
- sensors
- data
- arduino
- coding
---
![alarum](http://farm9.staticflickr.com/8345/8190530008_c57f2bcbb4_z.jpg)

Remember me getting [all excited about installing sensors around the Royal Shakespeare Theatre][1]? The commission I have been working on with [Caper][2] has been [unveiled yesterday][3].

[Alarum][4] is an ambient visualisation of the data showing changes in sound levels and motion around the theatre building.

The data often comes in every twenty to thirty seconds, depending on sensors' connectivity, so it needs to be analysed to decide which changes in sounds and motion level are meaningful. 

[Alarum][4] looks at average levels of data it receives. When these suddenly increase, it knows something has happened. If they continue at higher levels, it means activities continue in this part of the theatre. It is interesting to see how these change depending on time of the day, and how they change over the course of days and weeks.

[The raw data is available][5], so you can build something with it yourself. It would be great to see other projects made that look at it in a different way. Alarum's code is [on GitHub under the codename heartbeat][6], though it's so messy I am a bit embarassed to be sharing it.

![First sensor readings being received by Cosm](http://farm9.staticflickr.com/8180/7917689864_c40b54a5de_z.jpg)
_The first raw sensor data being received by Cosm_


[1]: 2012/09/14/sensing-activity-in-royal-shakespeare-theatre/
[2]: http://wearecaper.com/
[3]: http://myshakespeare.worldshakespearefestival.org.uk/gallery/alarum-by-natalia-buckley-and-caper/
[4]: http://alarumproject.com/
[5]: https://cosm.com/feeds/72813
[6]: https://github.com/ntlk/heartbeat