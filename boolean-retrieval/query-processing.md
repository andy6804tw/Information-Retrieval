# AND查詢處理

* 使用merge合併兩集合
  簡單來說分別有x、y兩串列，使用AND合併就是找出共同元素，相對的OR就是找出所有元素集合。

下面有個例子x、y集合，並使用AND合併，附帶JAVA程式碼:

x : 2、4、8、16、32、64、128  
y : 1、2、3、5、8、13、21



```java
import java.util.*;

public class Main{

	public static void main(String[] args) {

		int x[] = { 2, 4, 8, 16, 32, 64, 128 }, y[] = { 1, 2, 3, 5, 8, 13, 21 }, i = 0, j = 0;
		System.out.print("x AND y => ");
		while (true) {
			// 判斷i或j是否其中一個超出x、y陣列索引，若是則跳出
			if (i == x.length || j == y.length)
				break;
			if (x[i] == y[j]) {
				System.out.print(x[i] + " ");
				i++;
				j++;
			} else if (x[i] > y[j])// 若x[i]的值大於y[j]，j就加一
				j++;
			else if (x[i] < y[j])// 若x[i]的值小於y[j]，i就加一
				i++;
		}

	}

}
```
<pre>_Output:_
	x AND y => 2 8 
	
各位想想這樣的時間複雜度會是多少呢 ? 只有一個迴圈跑所以當時是O(x+y)。


