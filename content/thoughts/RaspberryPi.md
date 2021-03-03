+++
title = "RaspberryPi and Networking"
author = ["Alex Roos"]
publishDate = 2021-03-03
tags = ["linux", "network", "docker"]
draft = false
+++

The first RaspberryPi I bought was for my own Bitcoin/Lightning-Network node ([RaspiBlitz](https://raspiblitz.org/)). Building this project was a great learning experience and it introduced me to the idea of self-hosted software services.

## Using the RaspberryPi {#using-the-raspberrypi}

One of the first real use-cases I found for a RaspberryPi was to host my Telegram Bots. Since they require the running computer to be always online. Therefore, my solution to hosting bots written in [Python]({{< relref "learn2code" >}}) is to create a service on the Pi that executes the main script on start-up.

Another great practice was just to ssh into the Pi and do work from within the terminal. I found out about ssh-keys that way!

I also discovered, that [Doom Emacs]({{< relref "doom" >}}) allows me to ssh connect over [Tramp](https://www.emacswiki.org/emacs/TrampMode) and edit remote files on my local machine with my local config.

## My own home server {#my-own-home-server}

I have previously deployed my own [Nextcloud](https://nextcloud.com/) instance on a RaspberryPi, which taught me a lot about networking, port forwarding, SSL certificates and much more.

Moreover, the Pi has opened the world of docker for me!

Just as a side note: Nowadays I use a Pi as my home server and run [SyncThing](https://syncthing.net/) to keep all my `.org` files synced between my laptop and phone.

It truly amazes me that this tech exists at such a low price point!
