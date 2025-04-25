---
title: "Code Formatting"
date: 2025-04-04T16:53:18+01:00
draft: false
ShowLastMod: true
parent: DataDevops
summary: Introduction to Code Formatting
categories: Python
---

## What is Code Formatting?

Code formatting is the act of changing the format of your code
(such as line lengths, indentation, names of variables) according
to a set of pre-defined rules or styles.

It is just like the English language. We have rules that say
we add a 'full-stop' to mark the end of a sentence.

We add spaces between lines to demarcate a paragraph, which
indicates to the reader it is a new point to be made.

Code formatting is much the same. We indent underneath an
`if` statement to mark out all the code that will be executed
under the condition.

## Why should I format my code?

```
Imagine
if
I
started                         this
writing my blog like

                                        you would be
so
confused
        and
            read
              slower      it

```

If you tried reading the above, you will see the main point of formatting.
We follow standard formats because it enables us to read and absorb the information
in a fast and efficient way.

The key word is readability. It sounds boring but if you reflect upon
what happens if we don't organise round a common set
of rules - e.g. in the English language, in road signs, in Sign Language - then you
quickly realise how beneficial readability is.

## Style and Rule Guidelines

Given we now appreciate the value of code formatting, what styles or
rules should you follow and implement?

Well, just like human language itself, it develops a set of rules
over time as people see the value of them and either implicitly or
explicitly agree to using them.

So there is not usually an 'official' source of rules to follow, however most
of the programming languages tend to have a source or two that gather
consensus.

In `Python`, many of the rules and styles that are commonly followed
stem from a document called [PEP8](https://peps.python.org/pep-0008/#programming-recommendations). This document, written by Guido van Rossum
the creator of Python, lays out a broad set of guidelines covering things
such as:

- code layout (line length, indentation, import order, etc.)
- whitespace
- comments
- naming conventions

https://google.github.io/styleguide/
https://github.com/Kristories/awesome-guidelines

### Language Style Guides

Other languages have equivalent style guides. I've pulled out a few examples but
I'm not an expert, and I also found a useful Github repo that tracks all the style guides across all languages [here](https://github.com/Kristories/awesome-guidelines).

| Language   | Description                                                   |
| ---------- | ------------------------------------------------------------- |
| Go         | https://google.github.io/styleguide/go/                       |
| Python     | https://peps.python.org/pep-0008/#programming-recommendations |
| R          | http://style.tidyverse.org/                                   |
| Ruby       | https://rubystyle.guide/                                      |
| JavaScript | https://google.github.io/styleguide/jsguide.html              |

Ruff is both a linter and a code formatter

- PEP8 https://peps.python.org/pep-0008/#programming-recommendations
- List of formatters https://github.com/life4/awesome-python-code-formatters

## Code Formatters

Moving out of the theory, we can now talk about `code formatters`. These are tools
that seek to automate formatting according to these standard set of formatting rules.

Turns out there are [_loads of them_](https://github.com/life4/awesome-python-code-formatters). But the two most known at least from my personal
experience are `black` and `ruff`.

If you're interested to learn more, lookout for upcoming posts where I write a brief tutorial on both `black` and `ruff`.
