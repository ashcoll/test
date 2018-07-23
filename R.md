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
    * When a function calls another function, a new local symbol table is created for that call.
    * python中函数可以赋值。 (f = func1)
    * 函数可返回一个集合，比如List。如果函数没有返回值，则返回None。
    * More on Defining Fuprint(my_function.__)
nctions
        * Default Argument Values
            * def ask_ok(prompt, retries=4, reminder='Please try again!')
            * **The default values are evaluated at the point of function definition in the defining scope**
            * **Important warning:** The default value is evaluated only once. 
        * Keyword Arguments
            * Functions can also be called using keyword arguments of the form kwarg=value.
            * \*\*name is present, it receives a dictionary; \*name must occur before \*\*name.
        * 可变参数列表（Arbitrary Argument Lists）
            * These arguments will be wrapped up in a tuple.
            * def concat(*args) ...
        * Unpacking Argument Lists
            * \*-操作符会把list或tuple解压。
            * args = [3, 6]; list(range(\*args)); // 等价于 list(range(3,6)) == [3,4,5]
            * 如果是字典，使用\*\*来解压。
                * def parrot(voltage, state='a stiff', action='voom') ...
                * d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
                * parrot(\*\*d)
        * Lambda表达式
            * 小的匿名函数可以使用lambda表达式来创建。
            * Like nested function definitions, lambda functions can reference variables from the containing scope.
                * ```python
                    def make_incrementor(n):
                        return lambda x: x + n
                  ```
            * Another use is to pass a small function as an argument
                * pairs.sort(key=lambda pair: pair[1])
        * Documentation Strings(文档注释)
            * The first line should always be a short, concise summary of the object’s purpose. This line should begin with a capital letter and end with a period.
            * 如果文档需要多行，则第二行应空。隔开summary与description。
            * 从第三起，使用1个或多个段落来描述对象的调用约定、副作用（注意事项）等等。
            * python解析器并不会去除multi-line string（多行字符串）中的缩进，如果需要，应使用文档处理工具进行处理。
                * 第三行（简单来说）决定了整个文档的总缩进。不用第一行，因为第一行总是紧跟着三引号（"""）的。
            * Example             
            ```python
                def my_function():
                """Do nothing, but document it.
                
                No, really, it doesn't do anything.
                """
                    pass
            ```    
        * Function Annotations
            * Function annotations are completely optional metadata information about the types used by user-defined functions (see PEP 3107 and PEP 484 for more information).
            * Annotations are stored in the **__annotations__** attribute of the function as a dictionary. 
        
    



