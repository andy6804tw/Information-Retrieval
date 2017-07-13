# Skip pointers / Skip lists

先前第一章有提到兩個串列的合併，這個章節是要討論能夠在比較次數最少的時候，做出兩串列的合併，所使用到的是跳躍指標(Skip pointers)，另外必須注意一點是串列必須是有序的，也就是要先排序過。

#### Exercise2-1:

這題會給定一個數列，並依照題意算出找尋該數的次數

L1 : 4 6 10 12 14 16 18 20 22 32 47 81 120 122 157 180

(1): 47 using the standard posting list.

<pre>_solution:_<blockquote>
    這題是要你使用最簡單的方法逐一的從頭開始搜尋47所要的次數
    4->6->10->12->14->16->18->20-22->32->47<br>
    Ans : 11次

(2): 47 using skipped pointer skip length.

<pre>_solution:_<blockquote>
    這題是要你使用跳躍指標搜尋47所要的次數，其中跳耀的長度使用均等空間<br>√P(P代表串列的總長，故skip length=4)。走訪方式就一直跳躍當該數小於要被<br>搜尋的數值到大於時就往回到上一個節點逐一搜尋，如圖。  
    ![](/Img/exerxise2.1-1.png)
    4->14->22->120->32->47<br>
    Ans : 6次

