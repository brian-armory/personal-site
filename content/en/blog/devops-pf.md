+++
title = "What Personal Finance and Software Delivery Have in Common"
# subtitle =
tags = ['devops', 'finance']
date = 2021-01-13
description = "It might seem like an odd pairing, but software delivery and personal finance have a lot in common. Use personal finance principles to inform your software delivery."
banner = 'img/pf/gme-stock.jpg'
+++

![Gamestop stock, short sellers, and WallStreetBets collide](img/pf/gme-stock.jpg)

# Introduction

It's a new year. Many of us are setting personal resolutions and building out plans for the next quarter or year professionally. You don't have to look too hard to find "improving my personal finances" on someone's list of resolutions. If you're a software developer, you likely don't need to look too hard to find "DevOps" or something related to software delivery in an Objectives and Key Results (OKR) somewhere.

The best advice for both those things isn’t flashy or exciting. In fact, it's really boring.

Get rich quick schemes or expensive consultants that promise to revolutionize your software delivery lifecycle (SDLC) are a dime a dozen. But there is no secret sauce for personal finance. All the advice you'll ever need to be a personal finance savant fits on an index card (a concept made famous by financial journalist Helaine Olen and University of Chicago professor Harold Pollack). Software devlivery is the same.

When you look at personal finance, your money needs to make it from your paycheck (source) to your obligations (destination).

When you look at delivering software, your code needs to make it from commit (source) to your users (destination).

What's important for both isn't taking that big swing for a home run where you run the risk of "hit big or miss big." The graphic at the start of the blog post shows the volatility you open yourself to when you take that big swing. Show it to an average person and see if they have an appetite for that kind of risk when their money is on the line or the features that they're responsible for experience that kind of instability.

Instead, what is desirable but boring is this: take high percentage swings that almost guarantee you consistently good results. The incremental growth compounds on itself. We'll talk about ___the magic of compound growth___ soon, but first, the principles of personal finance and software delivery.

# Consistency, discipline, and repetition

**_Don't spend more than what you make_**

Charles Dickens and many others have given this advice. Simply put, make $20 and spend $19, you're golden. Make $20 and spend $21, you're setting yourself up for misery.

**_Make discipline easy by automating it and removing a variable, you_** 

We're all tempted _"buy"_ the shiny new object while running on a hedonic treadmill. Some of the most valuable companies in the world got that way because of how good they are at getting you to spend money. What's a person to do? The answer is to automate your savings. Contribute money to your 401k from each paycheck. Set up automated transfers to savings that work toward your goals. Do these things automatically. When temptation strikes, you'll be better equipped to resist because there's no money to spend. The extra money has already been tucked away safely.

_**Breath. Progress is incremental.**_

> _[Rule of 72](https://www.investor.gov/additional-resources/information/youth/teachers-classroom-resources/what-compound-interest)_
> 
> _Based on the rate of return, the rule of 72 estimates how long it takes to double a given amount of money._

Remember when I mentioned the magic of compound returns? If you take small swings in your 401k by investing in broad index funds, like SPY which tracks the S&P500, you can reasonably, safely, and sustainably grow your investments and wealth.


The S&P500 has averaged 10% returns (before inflation) over the course of its existence. Using the rule of 72, you can expect to double your money ever 7.2 years. Double your money with 0 effort on your part. It is that easy. It just takes time and patience.

*__Repeat the previous steps__* 

Consistency matters. That's it for this principle. It's the hardest one.

# What's this look like for software delivery?

**_Don't spend more than what you make == Don't overcommit_**

If you have 25 hours of actual hands-on-keyboard time, don't commit to delivering 40 hours of hands-on-keyboard features. You'll set yourself up for disappointing yourself, your team, and your customers.

**_Make discipline easy by automating it and removing a variable, you_** == **_Make discipline easy by automating it and removing a variable, you_**

Automate what you can. Configure your Continuous Integration (CI) system to scan for vulnerabilities and run integration and unit tests. Then, practice Continuous Delivery to make sure you can ship working software any time.

When the green field feature shows up, you'll be ready to jump in because you've set yourself up for success.

_**Breath, progress is incremental == Breath, delivering features and value is incremental**_

The next step after automating your vulnerability scanning and CI/CD process is to deliver changes that have a limited blast radius if things go wrong.

Your first iteration of a feature doesn't need to solve all use cases for everyone. Tackle a specific use case and solve it well. Grow from there after you've validated your feature with actual users. Put another way, remember high school physics?

> *F = ma*

That is, _force = mass * acceleration_. If given the option, would you rather deliver impactful changes by moving a heavy object (big feature) slowly or a small object (tightly scoped feature) quickly? I know which one I prefer.

_**Repeat the previous steps**_

Engineers like automating things. Bill Gates famously wanted to hire lazy engineers 'cause they'll find the easiest way to do something. The easiest way to repeat the previous steps is to automate them by software or established processes.

# Audit audit audit

For personal finance, this means you need to budget and track your spending.

For software delivery, this means tracking your sprint velocity to see if it matches with your time allocation.

# People first. Tools second.

It's hard doing the boring thing you know and being consistent about it. It's doubly hard when social media is talking about rockets, moons, and Wall Street Bets. On the software front, this is all the hyped up tech that FAANG companies (Facebook, Apple, Amazon, Netflix, and Google) love to talk about: cloud native, containers, Docker, Kubernetes, service meshes, etc.

Budgeting tools and tech stacks don't really mean much if the people who use them don't believe in and follow the behavioral practices and processes required. You're just adding overhead and operational complexity in those cases.

# Myths and gotchas

**The Latte Factor is bullshit.** For those unfamiliar, it's the idea that someone buying lattes for $5 is what's preventing them from becoming wealthy. More recently, this has been framed as Millennials buying $6 avocado toast is what's preventing them from buying a house.

Does spending $6 mean you don't have $6 to invest and benefit from the magic of compound returns? Yes, but this is really an overoptimization issue. It's really tempting to look at this low hanging fruit and think fixing this one little thing will cascade and solve all your problems. (It won't.)

Put another way, it's the idea of smelly code. The minor issue in the code (the "latte") isn't really **the** problem, but it can indicate a bigger problem that is actually meaningful. So let's fix the big problem instead.

**The income vs spending problem.** Here are some truths. What you can responsibly spend is directly related to your income. More income means more spending. There are costs associated with just being alive: food, shelter, clothing etc. To save more money, you can increase your income, decrease your spending, or both. For software delivery, it's the same. There are certain costs associated with building and maintaining software responsibly: fixing vulnerabilities, paying down tech debt, etc. You can increase the number of engineers, focus on specific priorities, or both. 

Which option do you choose? :shrug:

# Dive deeper

This blog post is a 10,000 foot view of how personal finance and software delivery overlap. We'll explore these more deeply in subsequent blogs. 

Have ideas about how other personal finance concepts apply to software delivery? Tweet @ [_brile](https://twitter.com/_brile) or file a [GitHub issue](https://github.com/brian-armory/personal-site/issues). Here's one topic already on my radar:

* Dollar cost averaging, lump sum investing & your DevOps

In the meantime, here are book recommendations if you want to go deeper into either the Personal Finance stuff or the DevOps stuff:

* _The Index Card: Why Personal Finance Doesn't Have to Be Complicated_ by Helaine Olen and Harold Pollack. It's a whole book! Or just search the internet for the actual index card.
* _Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations_ by Nicole Forsgren, Jez Humble, and Gene Kim

I have one really strong warning about either book though. When reading them, remember the section "People first. Tools second." Or really just that line.