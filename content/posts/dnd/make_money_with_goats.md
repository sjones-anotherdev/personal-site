+++
title = "Make Money With Goats"
date = "2022-09-16T10:17:04-04:00"
author = "Samuel Jones"
tags = ["DND", "Guide"]
description = "Making money with goats in DND 5e"
showFullContent = false
readingTime = true
hideComments = false
katex = true
+++
# Overview
So say you're with your party and you want to overthrow a king. Coups cost money, and you might not necessarily have as much as you might need. Behold, do I have a business proposal for you: goats. While each individual goat doesen't make much, it does add up over time. Here's how to make mone

# Prerequisite Information
All information you need is found in the PHB's [Equipment Section](https://www.dndbeyond.com/sources/phb/equipment#Equipment).
|          Item          |  Cost (gp)  |
| :--------------------: | :---------: |
|     Feed (per day)     |    0.05     |
|          Goat          |      1      |
|      Cheese, hunk      |     0.1     |
| _Hireling_ - Untrained | 0.2 per day |

# Calculation
- __The profit per goat is calculated as a function of time in days__: $ f(t)=0.05t - 1 $  
Where _t_ represents time.  

- __The total profit is calculated as a function of time in days__: $f(t)=G(0.05t - 1) - 0.2t \left\lceil \frac{G}{P} \right\rceil$
Where _t_ represents time, _G_ represents the total number of goats, and _P_ represents the number of goats per unskilled hireling.  

- __The profit per day is calculated as a function of number of goats__: $f(G) = 0.05G - 0.2 \left\lceil \frac{G}{P} \right\rceil$
Where _G_ represents the total number of goats and _P_ represents the number of goats per unskilled hireling.

# Estimated Profit
__With the number of goats per unskilled hireling as 30 and the number of goats as 100, the following function is used to estimate profits as a function of time in days__:
$ f(t) = 4.2t - 100 $
|   t   | f(t)  |
| :---: | :---: |
|   0   | -100  |
| 23.81 |   0   |
|  24   |  0.8  |
|  25   |   5   |
|  50   |  110  |
|  75   |  215  |
|  100  |  320  |