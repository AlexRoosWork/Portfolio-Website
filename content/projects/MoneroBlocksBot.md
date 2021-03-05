+++
title = "MoneroBlocksBot"
author = ["Alex Roos"]
publishDate = 2021-03-05
tags = ["python", "crypto", "telegram"]
draft = false
+++

> [Check the code out on GitHub!](https://github.com/AlexRoosWork/MoneroBlocksBot)

Once I had gotten the hang of programming a Telegram bot with the [ReputationBot]({{< relref "ReputationBot" >}}), I wanted to use this knowledge for something else.

## Playing with APIs {#playing-with-apis}

The purpose of this bot was for me to practice using public APIs.

Allthewhile I also wanted to provide some value to [Monero](https://www.getmonero.org/) ethusiasts on Telegram.

For this I used API provided by [MoneroBlocks.info](https://localmonero.co/blocks/api) (nowadays LocalMonero.co). With the right parameters in the URL you get a `json` object with the appropriate information (i.e. Block Height, TXs in the last Block etc.).

It was very easy to pull off with the `requests` module in Python.

## Running the bot as a service {#running-the-bot-as-a-service}

Another challenge when deploying the bot was to have it always running. After some asking around, I decided to let the Python script run as a service on my RaspberryPi. This way whenever my Pi is on and online, the bot would be running.
