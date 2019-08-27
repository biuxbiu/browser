## 变量
变量是用于存储信息的 `容器`，变量的值可以在整个程序中被修改。


#### 声明变量
```copy
var fruits;                         //通过 `var` 关键字来声明一个变量；
var fruites , color , price;        //也可以通过 `逗号` 隔开同时声明多个变量；
var fruits  = 'Banana';             //声明变量的同时可以给变量赋值;
var fruits = 'Banana',              
    color = 'yellow' , 
    price = '12';                   //可以一次性给多个变量赋值;
var fruits = 'Banana';              
var fruits = 'Apple';               //变量重名会产生覆盖;
```

!>声明变量需要注意以下几种情况

```copy
var fruits;                     //声明变量但是没有赋值的时候输出 `undefined`；
var fruits , Fruits;            //变量区分大小写， `fruits` 和 `Fruits` 是两个变量；
var fruits , _Fruits;           //变量命名需要语义化，以 `字母或者下划线` 开始；
var FruitsColor , 
    fruitsColor , 
    fruits_color;               //变量命名最好遵循大小驼峰写法或者下划线写发；

!>
var 12b = 'text';               //杜绝数字开头的变量（Invalid or unexpected token）
<!

```


#### 删除变量
用 `delete` 方法可以删除变量。
变量可以声明，也可以删除。<br>
删除变量要遵循以下几点：
* 所有 `var` 声明的变量都不可以删除（哪怕 `var` 的是全局变量）。
* 没有 `var` 声明的变量都可以删除。

<br>
<br>

<strong> 举个例子：</strong><br>

```copy
var x = 10;
y = 20;

delete window.x;        //false
delete window.y;        //true
```




#### 变量的存储与释放
在网页当中，浏览器都会把变量存储起来以便我们可以随时用到它。但是同时，浏览器也需要将它们释放，以免造成内存泄露页面崩溃。



##  总结
了解变量声明方式和规则，变量的覆盖。


通过 `var` 关键字来声明一个变量，可以通过逗号隔开同时声明多个变量，声明变量的同时可以给变量赋值，可以一次性给多个变量赋值，变量重名会产生覆盖

