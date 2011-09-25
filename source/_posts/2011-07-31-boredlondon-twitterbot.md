---
layout: post
title: Boredlondon Twitter bot
tags:
- twitter
- bot
- ruby
---

Part of my [final undergraduate project was][5] an experiment where I used a Twitter bot to reach a large audience in a short time. I wanted to see if people can be stimulated to action (and if so, how). [The source][5] is on Github, so you can have a proper look through it. [AeroFade][3]'s [bot which won][2] the [Socialbots][1] competition was a huge inspiration.

[@boredlondon][4] bot compiles a list of stuff to do in London from various rss feeds, with some free activities thrown into the mix. It then searches for people who say they are bored and (if their geolocation data points to London) it then introduces itself. If they reply (or mention the bot at all), it will give them a suggestion for a random activity.

[1]: http://www.webecologyproject.org/2011/01/help-robots-take-over-the-internet-the-socialbots-2011-competition/
[2]: http://www.webecologyproject.org/2011/02/complete-source-code-from-socialbots-2011/
[3]: http://aerofade.rk.net.nz/
[4]: http://twitter.com/boredlondon
[5]: https://github.com/ntlk/boredlondon
[6]: http://nataliabuckley.co.uk/projects/robots-against-routine/

Surprisingly, most of the interactions are very well natured and polite.

![](/images/boredombot1.png)
![](/images/boredombot2.png)

Though most of the bot's suggestions weren't what the participants could have hoped for.

![](/images/boredombot3.png)
![](/images/boredombot4.png)

It comes complete with rudimentary logging system:

{% highlight ruby %}
log.puts "---------------"
log.puts Time.now.to_s
log.puts "Tweeted: #{@message}"
{% endhighlight %}

One of the improvements I should have thought about when I began the experiment was to create a robust system for logging the whole history of bot's interactions, including the messages other people send to it. Because of the way the bot was written, its replies to mentions are not strictly _replies_ (they are not linked as a part of conversation), the bot remembers the names of people who talk to it and sends them a random suggestion (code fragment edited for clarity):

{% highlight ruby %}
mentions.each do |m|
  users = m.user.screen_name 
  users_that_replied << users
end
		
users_that_replied.each do |user| 
  random_tweet_including_free_stuff #returns @message
  begin
    Twitter.update("@#{user} #{@message}")
    follow_them = user.screen_name
    Twitter.client.follow(follow_them)
  end
end

{% endhighlight %}

This makes it very hard to archive the _conversations_, and sadly I haven't been doing it. I wish I had done it some other way. I would have been nice to keep track of how many replies are positive, negative, and rude; as well as noting down how many participants say they are likely to take up the suggestion. Any analysis and insights from the experiment seem anecdotal without the hard data to back it up.