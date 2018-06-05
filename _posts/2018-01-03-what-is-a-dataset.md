---
layout: post
title: Thoughts on Reference Data
published: true
---

Sets of records:

I have mentioned the word dataset a few times. Lets define that more specifically.

We'll start with an example. Lets say we have some stock ticker to company names records


Stock Ticker, Comapny Name

sd

sd

s

d


We might also have a table of stocks to addresses:


Stock Ticker, Company address

skdj

sd

sd


We can group these two tables and call them the stocks dataset. In practise, datasets would most likely contain many tables. Generally when we implement a database to hold datasets, we'll have one or more datasets within one dataset. Most likely we'll have only one dataset in one database. We'll rarely span one dataset across many physical databases. I've kept the terms separate because a database is a physical implementation, and a dataset is a conceptual grouping. Indeed it is possible to have a dataset be physically implemented as a set of CSV files in a folder on disk.
