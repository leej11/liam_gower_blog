---
title: "London Marathon: Rise in Popularity"
date: 2024-04-30T16:19:47+01:00
draft: false
plotly: true
tags: ["data", "hugo", "plotly", "Python"]
---

I saw recently that there were [record numbers](https://www.bbc.co.uk/news/uk-england-london-68918984) applying for the London Marathon. I myself am part of the problem as I put my name down this year :scream:.

And as it happens, I had previously pulled together the data on this and charted it. So here is an updated view as a Plotly chart!

{{< plotly json="/london_marathon_applications_accepted.json" height="400px" >}}

It almost seems to be increasing exponentially in the last few years! I wonder what the driver of its increasing popularity is?

One thing I might add to this chart is a line on a secondary axis that represents that applicant-accepted multiple. For example 2025 the multiple must be like 16x (16:1).

### How did I make this chart?

At work I'm forever making cool charts with Python, and so naturally I wanted to figure out how I could put similar charts onto my personal Hugo site here.

The chart is made in Python using `plotly` and then written out into `.json`. I won't go into the details here. In case you are interested, thankfully lots of other people have tackled explaining this already:

- [Rafa Marino](https://rafamarino.com/posts/plotly2.0/#2-conditionally-load-d3js-and-plotlyjs)
- [Mert Bakir](https://metalblueberry.github.io/post/howto/2019-11-23_add_plots_with_hugo_shortcodes/)
- [Mert Bakir](https://mertbakir.gitlab.io/hugo/plotly-with-hugo/)
- [ig248](https://ig248.gitlab.io/post/2018-11-05-plotly-sample/)

---

#### Sources

- [London Marathon Data](https://en.wikipedia.org/wiki/London_Marathon) - If anyone can find the missing years of 2021, 2022 and 2023 then please update wikipedia!
