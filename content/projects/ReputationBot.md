+++
title = "ReputationBot"
author = ["Alex Roos"]
publishDate = 2021-03-01
tags = ["python", "sql", "telegram", "sqlalchemy"]
draft = false
+++

> [Check the code out on GitHub!](https://github.com/AlexRoosWork/reputation-bot)

## My first real telegram bot {#my-first-real-telegram-bot}

Since I was an admin in a particular Telegram group, I wanted to use my programming knowledge to expand the utility of my group. Soon after, the idea for a Reddit-style voting bot for messages was born.

Basically, users have voting power that gets reset every 24 hours. Up- or downvoting consumes voting power. Users collect repuation over time and can "win the week", meaning that they are the user with the most upvotes in a given week. For every week championship a trophy emoji 🏆 is added to their reputation.

There are a couple more mechanisms, like leveling up. However, the goal was to incentivise the group members to post high quality content.

## Tying it all together {#tying-it-all-together}

With this programm I did my first steps with the [python-telegram-bot](https://python-telegram-bot.readthedocs.io/en/stable/) module. I experienced a steep learning curve and was also able to use my knowledge of SQLAlchemy to administer the database.
