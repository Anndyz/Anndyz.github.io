---
title: Javascript高程 第二章 使用Javascript
tags: Javascript
---
##### 本系列文章主要是用来记录学习Javascript高级程序设计的过程，是本书籍的课程笔记，这次笔记的内容则是第二章的部分
<!--more-->

- **script元素**

  ```html
  <script	>
  	//存在以下属性
      1.async defer 设置加载完毕异步执行与否
      2.charset 字符集 
      3.type  "text/javascript"
      4.src 其他地方引入js的源文件位置
      5.js是按照网页标签顺序解析的，如果都放在head标签内，会导致网页加载慢，现在一般是
        放置在body的结束标签之前
  </script>
  ```

  ​		**在html页面插入使用js，有以下两种方法**

  ​			**1.用script元素引入外部js**

  ​			**2.在script元素内部写入js，script元素可以在head内部，也可以在body标签内部**

  ​		**延迟加载defer**

  ​			**js脚本的执行需要等到文档所有元素解析完成之后，DOMContentLoaded事件触发执行之前。**	

  ​		**异步加载async**

  ​			**后续文档的加载和渲染与js脚本的加载和执行是并行进行的，即异步执行；**

