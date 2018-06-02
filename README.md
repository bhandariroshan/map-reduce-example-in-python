map-reduce-in-python
====================

Each file in the data archive contains entries that look like:  journals/cl/SantoNR90:::Michele Di Santo::Libero Nigro::Wilma Russo:::Programmer-Defined Control Abstractions in Modula-2.  that represent bibliographic information about publications, formatted as follows:  paper-id:::author1::author2::…. ::authorN:::title  

Task is to compute how many times every term occurs across titles, for each author.  
For example, the author Alberto Pettorossi the following terms occur in titles with the indicated cumulative frequencies (across all his papers): program:3, transformation:2, transforming:2, using:2, programs:2, and logic:2.  An author might have written multiple papers, which might be listed in multiple files. 

Further the ‘terms’ must exclude common stop-words, such as prepositions etc. For the purpose the stop-words that need to be omitted are listed in the script stopwords.py. In addition, single letter words, such as "a" can be ignored; also hyphens can be ignored (i.e. deleted). Lastly, periods, commas, etc. are ignored; in other words, only alphabets and numbers can be part of a title term: 

Thus, “program” and “program.” should both be counted as the term ‘program’, and "map-reduce" should be taken as 'map reduce'. There is no need to do stemming, i.e. "algorithm" and "algorithms" can be treated as separate terms.  

The task is to write a parallel map-reduce program for the above task using either mincemeat.py, each of which is a lightweight map-reduce implementation written in Python.
