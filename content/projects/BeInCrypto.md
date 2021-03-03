+++
title = "BeInCrypto Educational Telegram Bot"
author = ["Alex Roos"]
publishDate = 2021-03-01
tags = ["telegram", "python"]
draft = false
+++

> [Check the code out on GitHub!](https://github.com/AlexRoosWork/BeInCrypto-Telegram-Education)

## Using programming skills for real world value {#using-programming-skills-for-real-world-value}

In the summer of 2020 I was working as an editor in chief for the German section of [BeInCrypto](https://beincrypto.com/). While the work as a journalist and editor was certainly interesting and rewarding, by that time the passion to code had me already. So I wanted to program something that would be useful to the business.

As we grew our community, we started a Telegram group to onboard new users into Crypto. Since one of my responsibilities was to produce evergreen content and new crypto users usually start the same questions, my idea was to have a bot in our Telegram group that would give users a menu for all the evergreen articles we had to offer.

## Struggles when programming the bot {#struggles-when-programming-the-bot}

The actual code was easy to write. It was not my first Telegram Bot, and by then I had a pretty good graps on the [python-telegram-bot](https://python-telegram-bot.org/) module. However, my design was not the best, since it required hard coding of evergreen articles in the actual code.

With today's knowledge I would probably try to fetch the articles directly from the website. This way the code remains untouched, when new articles are released.
