---
title: Javascript高程 第三章 基本概念
tags: Javascript
---
##### 本次小记则是本书的第三章，主要介绍Javascript的一些基础概念、语法、数据结构、以及流程控制
<!--more-->

- **语法**

  ​		**1.区分大小写**

  ​		**2.标识符，就是指的是变量、函数、属性的名字或者函数的参数，有如下命名规则**

  ​				**2.1第一个字符必须是字母[abcd...]、下划线[_]或者美元符号[$]**

  ​				**2.2其他字符可以是字母、下划线、美元符号或者数字**

  ​				**2.3ECMAScript采用驼峰规则命名，比如myCar等等**

  ​		**3.注释：分为单行和多行注释**

  ​				**//单行注释**

  ​				**/* **

  ​							**多行注释**

  ​				***/**

- **语句**

  **Javascript语句以一个分号结尾**

  ```javascript
  var sum = a +  b				//有效语句，不推荐
  var diff= a - b;				//有效语句，结尾分号
  ```

- **关键字和保留字**

  ```javascript
  //关键字
  break case catch continue default delete do else finally for function if
  in instanceof new return switch this throw try typeof var void while with
      
  //保留字
  abstract boolean byte char class const debugger double enum export extends
  final float goto implements import int interface long native package private
  protected public short static super synchronized throws transient volatile
  ```

- **变量**

  **Javascript的变量是松散类型的，就是一个变量可以用来保存任何类型的数据，在这里，变量定义的关键字是 var，同时变量只在其作用域内有效**

  ```javascript
  var message = "hi";
  message = 100;				//松散类型，message从字符串类型指向了数字类型
  
  function test(){
      var message  = "hi";	//局部变量
  }
  test();
  alert(message);				//错误，在message的作用域外使用变量
  ```

- **数据类型**

  **ECMAScript有着5中简单数据类型，也就是基本数据类型：Undefined、Null、Boolean、Number、String，还有一种复制数据类型Object。**

  1. **Undefined类型**

     ```javascript
     var message;
     alert( message == undefined);		//true
     alert(message)						//undefined
     //定义了变量缺没有赋值时，变量默认为undefined
     alert(age)							//发生错误
     //未定义直接使用的变量，会产生错误
     ```

  2. **Null类型**

     **Null类型只有一个值就是null，null表示一个空对象指针，Null类型也是Object类型**

     ```javascript
     var car = null;
     alert(typeof car);			//"Object"
     //日常使用方式
     if(car != null){
         //to be continued
     }
     ```

  3. **Boolean类型**

     **Boolean类型是用来判断的，有两个字面量 true / false，和具体数值不对应，因此true不一定为1，false也不一定为0**

     ```javascript
     var found  = true;
     var lost = false;
     
     //进行判断的时候，可以由其他类型转型为Boolean类型的俩字面量true或者false
     ```

  4. **Number类型**

     ```javascript
     var intNum = 55;		//十进制
     var octalNum1 = 070		//八进制
     ....
     //浮点数
     var floatNum1 = 1.1;	
     var floatNum2 =3.12e7	//科学计数法
     
     //Number类型的数字存在范围，分别是Number.MIN_VALUE和Number.MAX_VALUE
     
     ```

  5. **String类型**
  
     **由单引号''和双引号""包含的字符序列**
  
     ```javascript
     var first = 'first';
     var second = "second";
     ```
  
     **ECMAScript中的字符串是不可变的，也就是字符串一旦建立，具体的值就不能改变**
  
     ```javascript
     var lang = "Java";
     lang = lang + "Script";
     //第二行的代码是，两个字符串拼接，然后变量lang指向了新的字符串
     //最后，在后台删除了这俩字符串
     ```
  
     **转换为字符串**
  
     ```javascript
     var age = 11;
     var ageAsString = age.toString();		//字符串11
     ```
  
     **Object类型**
  
     **Object类型是Javascript所以的对象的基础，所有的对象都具备Object所有的属性和方法**
  
     ```javascript
     var o = new Object();
     //1.constructor:保存着创建当前对象的函数，与类型同名，比如Object();
     //2.toLocaleString();返回对象的字符串表示，与执行的环境相关
     //3.toString()
     //4.valueOf()  
     //5.....
     ```
  
- **操作符**

  **一元操作符**

  ```javascript
  ++ --  + -  ~ ^ & << >>  ! &&  || ... 		//这类运算符只有一个操作数
  ```

  **多元操作符**

  ```javascript
  + - * / %
  ```

  