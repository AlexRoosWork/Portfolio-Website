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

The purpose of this bot was for me to practice using public APIs. Since I am passionate about cryptocurrencies I had the idea of creating a simple block explorer. One of my favorite coins is [Monero](https://getmonero.org) and so I started to dig. By far the simplest way of getting information on the Monero blockchain was [MoneroBlocks.info](https://localmonero.co/blocks/api) (nowadays LocalMonero.co).

The API could be queried with URL parameters. The result was a `json` formatted object. So, with the `requests` module in Python, I constructed the requests, read the information of the result and returned it to the user. The rest was simply tying Telegram commands to the appropriate functions.

While the bot is not a detailed block explorer to look up individual transactions, it still provides broad information, such as the current block height, the number of transactions in the last block, etc.
