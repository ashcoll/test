
### 1.1.2 jquery对象转换为dom对象

（1）jQuery对象实际上是一个数据对象，可以通过[index]方法获得相应的DOM对象。

如：var $v = ("#v"); // 得到jQuery对象

var v = $("v")[0]; // 转换成DOM对象

（2）jQuery本身可以通过.get(index)方法得到相应的DOM对象

如：var $v = $("#v");  // 得到jQuery对象

var v = $v.get(0);
