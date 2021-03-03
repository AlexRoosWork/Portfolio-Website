+++
title = "LevelUp - Tracking progress"
author = ["Alex Roos"]
publishDate = 2021-03-01
tags = ["python", "sql", "sqlalchemy"]
draft = false
+++

> [Check the code out on GitHub!](https://github.com/AlexRoosWork/LevelUp)

## My first real programm {#my-first-real-programm}

When I worked through "Automate the Boring Stuff", I wanted to keep track of my time invested in learning Python. So the idea for a timetracker with a command line interface was born.

It was a great exercise, because my knowledge on the first version was very limited. I did not use a database, but instead an Excel-Sheet, where I would automate the input into the cells, and read the cells to calculate my total time invested.

{{< figure src="/ox-hugo/level-summary.png" >}}

## Making improvments {#making-improvments}

As I progressed with learning the language and some modules, I revisited the application.

For instance, I used [Inquirer](https://pypi.org/project/inquirer/) for a neater menu structure in the command line.

However, the biggest improvement was certainly the switch from Excel to a SQL Database. Soon after I dropped the plain SQL and started to use the SQLWrapper [SQLAlchemy](https://pypi.org/project/inquirer/). This way the program is now database agnostic.

I also played around with [MatPlotLib](https://matplotlib.org/) to visualize progess over time in various views (last week, last month, all time etc.)

{{< figure src="/ox-hugo/matplotlib.png" >}}

## Summary {#summary}

While I don't use this programm anymore to track my invested hours, I still like it a lot. Not because of the functionality it provides now, but because of the lessons it taught me along the way.

I believe I had over 400 hours in Python when I quit using it.
