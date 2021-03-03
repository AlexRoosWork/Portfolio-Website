+++
title = "Python"
author = ["Alex Roos"]
publishDate = 2021-03-01
tags = ["opensource", "python"]
draft = false
+++

## Falling in love with programming {#falling-in-love-with-programming}

Python was the first computer language that I studied seriously. Over time I have fallen in love with the Zen of Python and learned a lot about broader principles of coding.

```nil
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

As I mentioned in [.#learn2code]({{< relref "learn2code" >}}), Python provides me actual utility. Early on I wrote a program to track my hours invested in learning the language. By now my window manger is configured with Python and I have many scripts to automate boring stuff.

## Learning to use framworks and read documentation {#learning-to-use-framworks-and-read-documentation}

Since the syntax of Python is fairly easy, I was able to focus on the important skills. Using any framework or module requires reading and <span class="underline">understanding</span> the documentation. This is a skill that I have developed greatly over the almost 2 years of teaching myself to code. Another is - of course - to use a search engine.

With the many modules Python has to offer, I was able to boost my own skills and developed several Telegram bots. My proudest achievement in this regard would be the [ReputationBot]({{< relref "ReputationBot" >}}).

## Customizing my desktop using Python {#customizing-my-desktop-using-python}

Nowadays, Python is my most comfortable language. As I mentioned, its functionality even comes into use on my own desktop. On my journey with tiling window managers, and after much frustration with [i3](https://i3wm.org/) and [awesome](https://awesomewm.org/), I discovered [qtile](http://www.qtile.org/).

Since qtile is written in Python the configuration is also a `.py` file. This means that I can write my own functions to feed the top bar widgets.

{{< figure src="/ox-hugo/topbar-qtile.png" >}}

For instance, the price of Monero and Bitcoin widgets I made myself. They are simply API calls to [Coinpaprika](https://api.coinpaprika.com/#operation/getTickers) packaged in a qtile widget.

```python
def get_cryptoprice(tickerid):
    """Query coinpaprika API for USD price. Return price as int."""
    url = "https://api.coinpaprika.com/v1/tickers/" + tickerid
    try:
        resp = requests.get(url)
    except:
        resp = '{"quotes": {"USD": {"price": "loading"}}}'

    data = json.loads(resp.content)
    price = round(data["quotes"]["USD"]["price"])
    return price


def get_xmr_price():
    price = get_cryptoprice("xmr-monero")
    return f'{price}{fa.icons["dollar-sign"]}'


def get_btc_price():
    price = get_cryptoprice("btc-bitcoin")
    return f'{price}{fa.icons["dollar-sign"]}'


def get_xmr_btc():
    """Calculate xmr/btc via usd price of both"""
    ratio = round(get_cryptoprice("xmr-monero") / get_cryptoprice("btc-bitcoin"), 4)
    output = f"({str(ratio)} btc)"
    return output
```

This is just one example of the many benefits, I draw from Python in my own environment.
