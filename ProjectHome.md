# RhymeDict #

The purpose of this project is to make a collection of _digitized_ texts of ancient Chinese rhyme dictionaries, and create human friendly tools for read, extraction and retrieval.


## guangyun\_skimmer ##

The first tool rolled out is a web application for local use --- [廣韻檢索](GuangyunSkimmer.md), by which you can browse or search entries of the most important Chinese RhymeDict Guangyun.

Expecting the broadest compatibility, this application requiring only the commonest features of a modern web browsers.(I developed it on ubuntu/firefox, other platforms and browsers are untested for now!)  All data from the original dictionary are converted into json format. RDBMS TABLEs are represented as a bunch of arrays, each one of them is comparing a column of a RDBMS table. A whole table is mapped to a js object with keys as field names and value arrays as columns. Unfortunately, the Arrays and Objects of javascript are pretty weak, it is very difficult to implement sorting or joining things like we do on RDBMS using SQL. It turned out,I can't create a **nomral** javascript application to serve common purpose dictionary searching, but I can make it serve one very particular purpose,namely Guankyun, I wrote a bunch of functions to fit the very dictionary. The data and the program merged together.

But I do keep the reusability in mind when I was developing this app. Despite the lameness, it does have some extent of flexibility, so it can be tweaked to fit another dictionary, even a collection of dictionaries, as long as the json data doesn't burst the browser's tummy!
