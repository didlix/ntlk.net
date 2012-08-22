---
layout: post
title: "Convert RGB to HSB (HSV) in Ruby"
date: 2011-11-21 19:40
comments: true
tags: 
- ruby
- colour value conversion
- rgb
- hsb
- hsl
---

I needed to convert RGB values into HSB. I found a very old gem, [colour-tools][1], which sadly only converts to HSL. So I rewrote [Alvein's C implementation][2] to calculate it in Ruby. Hope it saves someone time.

Inputs: red, green and blue values as integers between 0 and 255. Outputs according to HSB convention: hue as degrees (up to 360), saturation and brightness as percentages.

{% gist 1383603 %}

[1]: http://rubygems.org/gems/color-tools
[2]: http://forums.devshed.com/c-programming-42/rgb-to-hsv-conversion-rountine-162526.html