---
title: Poor error prevention. Stressful evening. Thanks a lot, Apple.
description: In a previous post I touched on Nielsen’s “10 Usability Heuristics for User Interface Design“...
date: 2016-07-01
layout: layouts/post.njk
---

In [a previous post](/posts/household-heuristics-why-a-flashing-light-is-good-ux/) I touched on Nielsen’s “[10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/)“. Though 20 years old, these nuggets still ring true.

Here’s a biggie:

> **Error prevention**:  
> Even better than good error messages is a careful design which prevents a problem from occurring in the first place. Either eliminate error-prone conditions or check for them and present users with a confirmation option before they commit to the action.

There’s more good stuff about [errors and how to prevent them](https://www.nngroup.com/articles/slips/) on the NNG site.

I recently fell foul of what I consider to be an inexcusable lack of error prevention.

Using Apple’s native Mail application on my Macbook, I searched for the out-of-office feature. It doesn’t exist (pity). Apparently I needed to set up a rule, to send a friendly message in reply to any incoming email, letting the sender know I’ll be sunning myself in Norway.

All good so far, and one final action for me to take:

![The offending window in MacMail - poor error prevention](/personal-site-11ty/img/Mac-Mail.png)<em>The offending window in MacMail – poor error prevention</em>

Sure, I was in a bit of a hurry to log off and go on holiday, but of course the choice was obvious – I clicked the welcoming blue button.

Two minutes later I got a call from my line manager, who was heading home on the train. His phone was going BING, BING, BING, BING, BING, BING, BING, BING, BING, BING – attracting the attention of other commuters, until he switched it to silent, but the emails had kept flooding in. 300 of them or so. (My only saving grace is that I’d only joined the company a couple of months previously, so the number of emails were limited.)

I retraced my steps and realised that that enticing blue button had applied my rule to ALL emails in my inbox, which meant a reply had been sent to EVERY email I’d EVER received letting my colleagues (including the CEO and various others) know I’d be on holiday.

I’m [not](https://discussions.apple.com/thread/3794748?start=15&tstart=0) – [the](https://discussions.apple.com/thread/6053279?start=0&tstart=0) – [first](https://discussions.apple.com/thread/4209073?start=0&tstart=0) – [person](https://discussions.apple.com/thread/4038511?start=0&tstart=0) this has happened to.

Apple die-hards may dismiss this as user error, and sure – I make mistakes like anyone now and again – but I maintain that this hugely embarrassing, unexpected consequence of such a common, ostensibly simple task was far too easily done.

The issues:

## 1\. Mail should have an out-of-office feature.

Debacle prevented.

## 2\. Why, why, why would I ever want the actions I took to lead to the results that occurred?

I cannot envisage a single reasonable scenario where any user would want to send the same reply to every single old email in their inbox. It simply shouldn’t have been possible for this to happen.

## 3\. It shouldn’t have been so easy.

Even if it had to be possible (which it didn’t), it was far too easy for me to click that button, considering the seriousness of the results.

There’s plenty of research about [how little people read online](https://www.nngroup.com/articles/how-little-do-users-read/), and the impact and [psychology of colours](https://www.paulolyslager.com/call-to-action-buttons-psychology-color/). So, 100% scientifically, this is what my brain processed when I saw that confirmation window:
 
![UX - how the brain processes colours and text](/personal-site-11ty/img/Mac-Mail-blurred-JPEG.jpg)<em>Scientifically, what my brain processed</em>

Putting aside the issue that this result shouldn’t have been possible in the first place, there are options which might reduce the likelihood of errors.

For example:

*   swapping the buttons, to make ‘Don’t Apply’ the default
*   showing ‘Apply’ as text (rather than a button) to further distinguish it from the preferred option
*   adding a warning symbol and/or warning explanation to ‘Apply’
*   rewording the window to make the action and consequences clear (the copy at the moment is very unclear, in my view) and changing the wording on the ‘Apply’ button to something more specific like ‘Reply to every single email in your inbox, even though you’d never ever want to do so’ (er… or maybe something a little more concise)
*   A confirmation ‘Are you sure?’ pop-up, or the option to undo before the changes kick in.

And so on.

## 4\. Users hate errors

When poor system design leads to serious consequences for the user that could and should have been avoided, that’s about as frustrating as it gets in terms of user experience. Error prevention isn’t the most glamorous part of UX but there’s nothing more important.

I’ve stopped using Mac Mail.
