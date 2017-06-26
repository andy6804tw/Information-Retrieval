# 反式向量 Incidence vectors

* 文件少、相似度高時較有效率

* Incidence vetors顧名思義就是以向量\(0與1\)表示文件的有無

### Exercise1:

![](/Img/exercise1.png "1123")  


Q1.1: Brutus AND Caesar but NOT Brutrs

<pre>_solution:_<blockquote>
    Brutus  => 110100
    Caesar  => 110111
    !Brutrs => !(010000)=>101111  
    ![](/Img/exerxise1.1.png)
    
    
Q1.2:Calpurnia OR mercy but NOT Brutus

<pre>_solution:_<blockquote>
    Calpurnia => 010000
    Mercy     => 10111
    !Brutrs   => !(010000)=>101111 
    ![](/Img/exerxise1.2.png)