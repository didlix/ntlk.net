---
layout: post
title: "Sensing activity in Royal Shakespeare Theatre"
date: 2012-09-14 07:25
comments: true
tags: 
- arduino
- sensors
- rsc
- pir
- electret mic
- sound
- noise
- motion
- iot
- electronics
- data
---

![Motion Sensor in the Swan Bar](http://farm9.staticflickr.com/8297/7918060170_84de124234_z.jpg)
_Noise level sensor in the Swan Bar_

Together with [Caper][2] I have also been working on a small art project for the RSC. We've been interested in working  with the [building itself][3]. Visitors tend to come to Stratford-upon-Avon for the evening, enjoy the performance, perhaps some food and drinks, and head back, often on the next day. As well as the audience, there are also people working front of house, behind the bar, not to mention the three different acting troupes working on stage. 

We wanted to explore the building as a whole, the total sum of effort and action that makes experiencing the performance possible; some of it behind the scenes. To do that, we wanted to put together an app that would analyse, visualise and display activity in the building as it happens.

But how do you measure activity? You could look at the amount of stuff made, amount of waste generated, or resources used up, but to measure life you have to measure its symptoms, like noise and movement. We wanted to put sensors in the theatre to make the often invisible efforts plain to see. To be able to say: at noon on Wednesdays the wardrobe rooms get very busy; that here is a sudden burst of activity backstage on Thursday morning when the set gets installed; that the bar is actually busiest on Monday nights.

I have prototyped two types of devices: motion and sound sensors. Both use Arduino Ethernet boards to send data to [Cosm][13], which I am using both to make the feeds publicly accessible, and to set up triggers that will communicate with a web app built to analyse and visualise the data. I had thought of making my own Arduino-compatible boards to save money, but there simply wasn't enough time to make that possible.

![Motion sensor device](http://farm9.staticflickr.com/8453/7917442134_5fc67fd717_z.jpg)
_Motion sensor_

The motion sensor devices are very straightforward: simply plug in an infrared motion detector in to start logging. The time it takes for the sensor to keep sending the signal about the detected movement can be adjusted. I add every positive reading to a counter, and send the total to Cosm every 30 seconds.

Sound sensors initially seemed trickier, though I only needed to measure the levels or determine that they are over a certain threshold. My first approach was to try and use [piezos][14] positioned on the floor or frequently used flat areas (such as the bar) to detect surface vibrations. Piezos are sensors that can detect pressure and vibration (and thus sound) and are often used as guitar pickups. I found it very difficult to amplify the piezo signal enough to turn it into a sensitive sensor over a large area though. 

This is of course possible. Another member of the local hackspace, [Jason Hotchkiss][5], has built [exactly the kind of sensitive piezo sensor][6] that I had been thinking about. He designed and built all the electronics that went into this [musical ping pong table][8]. I attempted to recreate Jason's sensors, though I have used a completely different [op-amp][9] and my results didn't come anywhere close. 

Another approach I've tried was using an electret microphone with a [cheap DIY amplifier I found on Alex Weber's blog][7]. This time I didn't have the right transistor, and though I had some that _apparently_ could be a substitute it still got me nowhere: readings were full of noise and their range wasn't good enough. Though I have a huge range of completely random components lying around it turns out I don't actually have much useful stuff. Also I still suck at analogue circuits.

As I waited for the right components to show up in the post, with the deadline fast approaching, I had to explore other options. A basic amplifier isn't exactly very difficult, and the inability to actually get a working one made was making me very frustrated, but in the end I had to go for the off-the-shelf solution as I had to install the devices the very next day. I used Sparkfun's electret mic with an amplifier on a breakout board, ready to simply plug in and play. Not only I am embarrassed at my failure to prototype something basic, but also at the fact that I am using components that are probably 8-10x more expensive than strictly necessary. 

![First readings coming in](http://farm9.staticflickr.com/8180/7917689864_c40b54a5de_z.jpg)
_First sensor readings coming in_

But hey, the devices worked and that's what matters, right? I've laser cut some dashing boxes to protect them, ready for the installation in situ. Motion ones were placed near Stage Door and in the Wigs & Wardrobe department, sound ones in the Green Room and in Swan Bar.

Something I didn't think about when prototyping the devices was giving them some way of communicating with their surroundings, namely reporting that they are connected and everything is fine, or that there is an error of some kind and they would need to be reset. The switch that allows resetting them would also be great to have on the outside of the box.

Another thing that I have only seriously considered while installing the devices was communicating what they do to people working at the theatre. I think I would have appreciated more time spent on location talking to people about the project, especially the fact that these aren't cameras or recording devices - it's impossible to know this just by glancing at them. It would have been impossible to speak to the entire 700 strong team though, so we've put up notes explaining a little bit about the project and displaying some sample data from Cosm. There must be a better approach to communicating their purpose and how they work though. 

The sensors have been collecting data for nearly two weeks now. I've built a sample Rails app that is dealing with the interpretation of the readings, which need to be analysed and calibrated before going live.

You can [see the data for yourself on Cosm][4] (formerly Pachube). I encourage you to pull it and do something interesting with it. I'd be very interested to see what else it can be used for. 


[1]: http://www.rsc.org.uk/whats-on/exhibitions/recoding-shakespeare.aspx
[2]: http://wearecaper.com
[3]: https://en.wikipedia.org/wiki/Royal_Shakespeare_Theatre
[4]: https://cosm.com/feeds/72813
[5]: http://hotchk155.blogspot.co.uk/
[6]: http://hotchk155.blogspot.co.uk/2011/10/musical-ping-pong-tables-and.html
[7]: http://tinkerlog.com/2007/05/20/cheap-sound-sensor-for-avr/
[8]: https://vimeo.com/45745840
[9]: https://en.wikipedia.org/wiki/Operational_amplifier
[10]: http://www.rsc.org.uk/
[11]: http://myshakespeare.worldshakespearefestival.org.uk/
[12]: http://worldshakespearefestival.org.uk/
[13]: https://cosm.com/
[14]: https://en.wikipedia.org/wiki/Piezoelectric_sensor

