---
published: false
---
Something that a master reference database can contain is master lists. A master list is a set of records that enumerate a set of known and desired things. Lets continue using the example of stocks.


We can create a list of stocks that we care about as a set of records containing their tickers:


Stocks Table


Ticker:

slhs

d

dsd

s

d



We can place in this list all the stocks that we care about, or know about. Specifically, this then then becomes the intersection of the list of stocks that we know about, and the list of stocks that we care about.

Crucially, we want entries of this list to be unique. Having duplicates could issues when trying to some types of analysis using the list. For example joining the master list of stocks with trading profit and loss items. We could end up double counting profits for the same stock.

This list can then be queried. Eg: 

"Give me all the stocks whose ticker begins with 'A' "

In the scope of a master reference database, we want the "stocks" list to contain all a master list of stocks and contains the definitions of the stocks for a given scope (usually  the enterprise).


Master lists are extremely important as they often form the basis for many queries. One might query, for all the stocks that don't have prices for yesterday. If one didn't have a master list, one would most likely have to create a list of stocks of interest from the set of the prices from the day before. This is time consuming and prone to errors. Some stocks might have been suspended and have no price for the day before. Building master lists is a key component of building a reference database.


To do this we need to ascertain the scope (what stocks do we need / want), and the sources (where can we get lists of stocks). Often, we will need combine multiple sources of lists into one. This then throws up the next problem of ensuring that we don't end up with duplicates. This is a significant challenge in many areas. We'll need to have a think about natural keys to do this.
