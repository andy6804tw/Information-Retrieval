# 反式索引 Inverted index

* 優於陣列
* 動態空間配置\(Dynamic space allocation\) =&gt; Postings lists

### 反式索引建立 Inverted index construction

![](/Img/Image05.png)

如上圖各位可以看到這是整個索引建立的流程，首先取得文件，再來利用Tokenizer把文件做切割形成每一個term\(單字的意思\)，這邊切割是把每個單字切出來，接著使用正規化把每個單字轉成遠使型態\(大寫-&gt;小寫、s去掉、複數-&gt;單數\)，最後步驟就建索引，記住字母排序是件索引檔最複雜的地方。

### 索引步驟 Indexer steps

1. 單字依序放入串列
2. 依照字母序來排序 \(排序是建索引最核心的地方\)
3. 重複字合併，新增頻率資訊
4. 建立各文章出現次數頻率


#### Exercise1-5:
![](/Img/exerxise1.5.png)<br>

(1)Draw the term –document incidence matrix
<pre>_solution:_<blockquote>
    題目是要你寫出每個單字term發生次數的矩陣，故如下圖<br>
    ![](/Img/exerxise1.5-1.png)

(2)Draw the inverted index representation
<pre>_solution:_<blockquote>
    題目是要你畫出Postings lists，故如下圖<br>
    ![](/Img/exerxise1.5-2.png)

(3)query  schizophrenia AND drug
<pre>_solution:_<blockquote>
    schizophrenia => 1111
    drug          => 1100<br>
    ![](/Img/exerxise1.5-3.png)

(4)for AND NOT (drug OR approach)

<pre>_solution:_<blockquote>
    這題稍複雜，查詢for和非(drug或approach)
    for                  => 1011
    drug                 => 1100         
    approach             => 0010
    !(drug OR approach)  => !1110 => 0001<br>
    ![](/Img/exerxise1.5-4.png)





