# Phrase queries
* 片語查詢(Phrase queries)主要有兩種


1. 雙字索引(Biword indexex)
2. 位置索引(Postitional indexex)

### 雙字索引(Biword indexex)

缺點:字典變大<br>優點:節省搜尋時間，兩字一組<br>①去除死字<br>②只對名詞做biword

ex: cost overruns on a power plant<br>
=> Biword (cost overruns) (overruns power) (power plant)

### 位置索引(Postitional indexex)

< be: 993427 <br> 1: 7,18,72,86,231;<br>2: 2,149;<br>4:17,191,291,430,434;5: 363,367; ...>

ex: to be or not to be 可能出現在Doc4、5，因為片語中兩個be相差3個距離<br>
故位置索引可做接近查詢。

#### Exercise2-3:

Assume a biword index. Give an exmple of a document which will be returned for a query of New York University but is actually a false positive which should not be returned.

<pre>_solution:_<blockquote>
    New York University使用Biword
    <br>
    Ans: biword(New York)AND(York University)
    
    
#### Exercise2-4:

使用位置索引查詢下列片語可能在哪幾個文件當中
![](/Img/exercise2.4.png)

(1): fool rush in

<pre>_solution:_<blockquote>
    Ans: Doc 2、4、7
    
(2): "fool rush in" AND "angles fear to tread"

<pre>_solution:_<blockquote>
    Ans: Doc 4

#### Exercise2-5:

Are the following statments true or flse?<br>
a. In a Boolean retrieval system, stemming never lowers precision.
b. In a Boolean retrieval system, stemming never lowers recall.
c. Stemming increases the size of the vocabulary.
d. Stemming should be invoked at indexing time but not while processing a query.
<pre>_solution:_<blockquote>
    Ans: a. False
         b. True
         c. False
         d. False
