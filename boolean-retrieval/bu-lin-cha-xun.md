#布林查詢
* 使用AND、OR、NOT做多條件搜尋

disjuction → 聯集 、 conjunction → 交集

_布林式_

1. ( A OR B ) AND NOT ( C OR D )<br>
    
    (A+B) * !(C+D) = (A+B) * !C * !D
    
<p>
Q1: Can we aleays merge in linear time?
    <pre>_Ans:_
    有可能。
    
Q2:Can we do better?
    <pre>_Ans:_
    Linear in posting list length。

    
