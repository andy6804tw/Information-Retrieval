# 精確率和召回率\(Precision and Recall\)

**除了精確(Precision)還有一個叫準確(Accuracy)那我們來提一下這兩個名詞的區別**
我們以打靶上的靶紙作為解說例子如下圖，紅色為射擊點，您可以在左圖中看到射擊點都有落在目標物靶紙圓上這就是準確，然而右圖是射擊點都集中在某處(當然不一定都要圓心，只要夠集中就好)這就是準確。

![](/Img/Image03.png)


那看到這裡問問各位，準確好還是精確好呢 ? 當然是越精準越好啦~
以下就由式子和例題來帶各位了解精確和召回吧 !


![](/Img/Image04.png)

#### Exercise1-1:

假設在資料庫有1000筆資料，和美食有關文章有500篇，使用者在輸入美食關鍵字後，回傳的文章有4000篇，其中有400篇是和美食有關的，請求出精確率(Precision)和召回率(Recall)。
<pre>_solution:_<blockquote>
![](/Img/exerxise1.1.png)



#### Exercise1-2:
資料庫有500筆資料，符合需求的原有45筆，如果查詢筆數設定輸出50筆時，有23筆符合需求，請求出精確率(Precision)和召回率(Recall)。
<pre>_solution:_<blockquote>
![](/Img/exerxise1.2.png)


#### Exercise1-3:
1000筆資料15筆是符合資料，設定Tr(取出個數)Tc(取出符合的個數)，請求出精確率(Precision)和召回率(Recall)。

(1) Tr=10 Tc=7
<pre>_solution:_<blockquote>
![](/Img/exerxise1.3-1.png)

(1) Tr=12 Tc=10
<pre>_solution:_<blockquote>
![](/Img/exerxise1.3-2.png)







