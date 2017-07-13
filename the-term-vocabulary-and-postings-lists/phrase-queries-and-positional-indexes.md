# Phrase queries
* 片語查詢(Phrase queries)主要有兩種


1. 雙字索引(Biword indexex)
2. 位置索引(Postitional indexex)

## 雙字索引(Biword indexex)

缺點:字典變大
優點:節省搜尋時間，兩字一組
①去除死字
②只對名詞做biword

ex: cost overruns on a power plant
=> Biword (cost overruns) (overruns power) (power plant)