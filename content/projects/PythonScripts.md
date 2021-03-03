+++
title = "PythonScripts - Automate the boring stuff"
author = ["Alex Roos"]
publishDate = 2021-03-01
tags = ["python", "linux"]
draft = false
+++

> [Check the code out on GitHub!](https://github.com/AlexRoosWork/PythonScripts)

Here I have 3 different Python scripts that automate certain aspects of my workflows.

## delete_txts.py {#delete-txts-dot-py}

When I coded my first lyrics grabber for iTunes, I had saved the lyrics for all songs in the album direcotry as a `.txt`.

This was not necessary, but it didn't bother me much at first. However, since my library contains around 7.000 songs, I also had 7.000 `.txt` files just lying dead, nested in the library directory. When copying/backing up this folder, the number of files slowed down the process considerably.

Instead of deleting all `.txt` files manually, I wanted to automate that boring stuff.

This was a good exercise to get more familiar with the [os module](https://docs.python.org/3/library/os.html) in Python, especially the `os.walk()` function.

## filesorter.py {#filesorter-dot-py}

Another usecase that cried to be automated was sorting through an older directory. Sometimes I just dump files in a directory so not to delete them. But this bad habit accumulates a lot of unsorted files over time.

So this `filesorter` goes through any given directory, scans all files, creates directories for every extension and moves the files into the appropriate directory.

A great way to clean the `Downloads/` directory!

## pdfsorter.py {#pdfsorter-dot-py}

Another way to get my stuff in order. This script asks for a directory, then gets all the `.pdf` files and opens them one by one. The purpose is to give meaningful names to the pdf and then move it to a directory named after the year the `.pdf` was created.

This way I organise my documents and have everything named appropriately, when I do my taxes.

## Summary {#summary}

Writing scripts like these make feels really rewarding. I am able to automate my operating system and create my own custom workflows. During my use I came to discover [PyInquirer](https://github.com/CITGuru/PyInquirer#installation) to create beautiful menus in the command line interface.

Another perk is that it takes me very little time to write these scripts now, since I am more familiar with the `os` module.
