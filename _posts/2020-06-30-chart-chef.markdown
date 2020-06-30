---
layout: post
title:  "Chart chef - side project on trading"
date:   2020-06-30 08:00:00 +0300
categories: tech
tags: side-project charting trading technical analysis
---
## The WHY
Technical analysis and trading have always drawn my interest. They are the crossroad of money, behavior and psychology. The unprepared 👁 sees colorful lines on the 📈📉. The prepared one sees fear and greed all over.

Majority of people lose 💰 trading. Few are profitable. Very profitable. Don't know the actual distribution but I would say that is close to Pareto principle. 80% lose money, 20% profit. 20% of the profitable ones make 80% of the profits.

Why so? I believe the reason is 🧠 and **practice**. Trading involves 🧠 but practice is so much more important. This is a "gets hands dirty" thing or rather "bust a few trading accounts" thing.

I enjoy staring at charts, following price action and observing whether my interpretations play out.

I was lacking a good tool to sharpen my skills and decided to build one for myself.
🥁🥁🥁[CHART CHEF](http://www.chartchef.com/) 🥁🥁🥁.

## The WHAT

A picture days a thousand words.

<img src="/assets/chartchef.png" alt="Chart chef screenshot">

The initial load pulls a random stock in a random time frame and draws a chart. Then, you can buy/sell, progress to next day or just draw another chart. When you buy/sell and progress, your account balance changes. The goal is to make 💰. Simple, ah?

Speaking of charts, you can make them as complex as you like. There is no limit. Just go check out trading view and you will get a notion. I decided to keep it simple. Price, a few moving averages, volume and a simple interface.

## The HOW

In terms of tech stack this is super easy and straight forward. Here is what I use:

* Ruby with Sinatra on the back end. My web serving code is very short. < 100 lines at the time of writing.
* Postgres to store stock data
* Yahoo finance free API to fetch price data. I fetch and store data with rake task.
* JS, HTML, SCSS on the front end. Vanilla JS with jQuery. Bootstrap for layout. No other frameworks. I can go even without Bootstrap and jQuery but played it lazy.
* [Tradingview's lightweight chart](https://github.com/tradingview/lightweight-charts/). Picking a charting library was the hardest. This one is very lightweight (duh, it is in the name 😃) and has enough features to get you started. It is free and open source.
* Heroku hosting. For now free but I feel I have to pay for DB as now i get only 10k rows of DB data.
* Namecheap for domain. 7$ spent on that.

I want to keep things really simple as a beginning and add stuff as I iterate and gather feedback. All in all, I spent about 2 full time days on this one or ~ 16 hours and it is up and running.

The code is a hot mess (of course 😊). But code quality can wait for now. It can wait until, I have users, I need more features, I have a clearer vision on the tool etc etc. Pretty much last concern. Not that I don't care. But in an environment of scarce resource (time in this case), it can wait.

Enjoy and hey, reach out and say 👋 if you like it. I will be glad.
