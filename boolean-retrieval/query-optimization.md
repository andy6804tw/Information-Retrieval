# 查詢優化 Query optimization

* 可以透過處理順序把速度加快
* 第一、二大先合，最後再合最小的

A : 2、4、8、16、32、64、128
B : 1、2、3、5、8、16、21、34
C : 13、16

( A AND B ) AND C
但也有人說( B AND C) AND A 才是最快，這是蠻值得討論的議題。

## 窮舉法 Heuristic

好的解法 : 交集兩最小的posting list

#### Exercise1-6:
A : 46653
B : 316812
C : 107913
D : 271658
E : 87009
F : 213312

<pre>_Ans:_
( E OR F ) AND ( A OR B ) AND ( C OR D )
  300321         363365         379571
  
#### Exercise1-7:
If the query is friends AND romans AND (NOT countrymen),how could we use the freq of countrymen ?

  <pre>_Ans:_
  使用現有最大頻率當n
