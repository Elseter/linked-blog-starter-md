
---
aliases: [ "20221028110252",  ]
tags: RWU, COMSC.110, COMSC, Programming
date_created: 2022-10-28 11:02
---
[[COMSC.110 INDEX]]
# Multidimensional Arrays
---
## 2 Dimensional Arrays
- Will have one variable title (name)
- A collection of collections of data
- Data must be all the same type
- row-index is 0-based
- col-index is 0 based
- <u>FIXED SIZE</u>
- ==myData.length variable will now return the number of rows==
- ==myData[0].length will return the length of the row==
#### Declaration code
```java
int[][] myData = new int[4][3]; 
// 4 is the number of rows  
// 3 is the number of columns  
myData.length // will return 4  
myData[0].length // will return 3
```
