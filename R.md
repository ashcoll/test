# Python3.7 tutorial

## 3. An Informal Introduction to Python

### 3.1.1. Number

* division always returns a floating point number
* 整数与浮点数混用，会转化为浮点数
* multiple assignment： a, b = b, a+b

### 3.1.2 String
1. Python中，字符串可以使用单引号或双引号，也可以使用3个单引号或双引号表示多行字符串。
1. 转义字符使用"/"，或者在字符串前使用r（比如r"C:\some\name")表示raw string）
1. 字符串可以使用“+”号连接
1. string也可以使用下标引用（从0开始）
    1. 下标也可以为负数，表示从右引用，-1表示最左边的元素。（-0 is the same as 0）
    1. 也可使用word[0:2]形式进行字符串截取。（包前不包后）
1. python中，string为不可变对象。所以使用下标改变string中的元素是不行的。


### 3.1.3 List
1. python中没有数组，可使用List集合代替
    * squares = [1, 4, 9, 16, 25]
    * index: squares[1] 
    * +: squares + [36, 49, 64, 81, 100]
    * cubes.append(216)
    * nest list - [['a', 'b', 'c'], [1, 2, 3]]
    * 浅拷贝-squares[:]: returns a new (shallow) copy of the list.
        * 拷贝squares中的元素，如果squares中有元素也是个list，则只拷贝引用。


## 4. More Control Flow Tools
1. if … elif … elif … else
1. for Statements
    * for var in collection
1. The range() Function - iterate over a sequence of numbers
    * range(5, 10)  # 5, 6, 7, 8, 9
    * range(0, 10, 3)  # 0, 3, 6, 9
    * range(-10, -100, -30)  #-10, -40, -70
    * list(range(5))  #[0, 1, 2, 3, 4]
1. **break** and **continue** Statements, and **else** Clauses on Loops
    * The break statement, like in C, breaks out of the innermost enclosing for or while loop.
    * else - Loop statements may have an else clause
        * 循环遍历完或条件变为False(while)时，执行else块。break结束循环时不会执行else块。
        * a **try** statement’s <span style="color:blue;">else</span> clause runs when no exception occurs。
    * The **continue** statement, 与c相同。
1. pass Statements
    * pass语句不做任何事；常用来在空代码情况下保证语法正确。
1. Defining Functions
    * 使用def关键字
    * All variable assignments in a function store the value in the local symbol table;whereas variable references first look in the local symbol table, then in the local symbol tables of enclosing functions, then in the global symbol table, and finally in the table of built-in names.
    * Global variables cannot be directly assigned a value within a function (unless named in a global statement).


    





