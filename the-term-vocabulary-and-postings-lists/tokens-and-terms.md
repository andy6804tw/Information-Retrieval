# Tokens and Terms
* 在索引裡面，字典越小越好，要縮減字典裡的字

### Tokenization
把一句話切成token(連接詞、介詞捨去)
Friends, Romans and Countrymen
<pre>_Output:_
    Friends
    Romans
    Countrymen
    
這裡要思考的是所有單字都是要這樣以空白切開嗎?並不全然!
例如國家地區:San Francisco
若切開兩個單字並無意義了

###Number

數字是非常難去判斷切割的每個地區或國家都有習慣的呈現方式
例如日期:
3/12/91
Mar. 12, 1911
55 B.C.
B-52

### Stop words

the、a、and、to、be這些都是介詞、貫詞、連接詞
所以在字典中可以不必出現，一方面可以減少字典大小。
不過這也是要取捨的萬一這些名詞是有意義的片語呢?
ex : To be or not to be、Let it be



### Normalization 正規化

目的 : 減少字典大小。
優點 : 不用去查詢字典。
缺點 : 資訊變多，資訊變資料。

### Case folding 大小寫統一

不是所有字都可以轉小寫，因為有些情況必須保持大寫。ex: USA。
目的 : 減少字典大小。

### Synonyms 同義字

car = automobile 
以人工去建，對等關係，當輸入某一個字詞時，會查詢到她的同義字。

### Homonyms 同音字

名的音接近但字不同，當不同的字發出聲音非常接近的時候，那些字會變同一組碼

### Lemmatization 標題化

目的 : 減少字典大小。
am、are、is → be
car、cars、car's → car

ex:
the boy's cars are different colors
→ the boy car be different color

### Stemming 抽梗

* 將字回歸最原始

ex:
for example compressed and compression are both accepted as equivalent to compress
→ for exampl compress and compress ar both accept as equival to compress

### Porters's algorithm

將單字回歸原型並依依照下列規則 :<br>
sses → ss<br>ies → i<br>ational → ate<br>tional → tion<br>ss →s<br>s → 去除<br>
ex:<br>caresses → caress<br>ponies → poni<br>caress → cares<br>cats → cat
