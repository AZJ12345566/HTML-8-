# HTML-8-
HTML类 ld 内联框架
//HTML类
  //对HTML进行分类(设置类)，使我们能够为元素的类定义CSS样式
  //为相同的类设置相同的样式，或者为不同的类设置不同的样式
  //实例：
  <html>
  <head>
  <style>
  .cities{
    background-color:black;
    color:white;
    margin:20px;
    padding:20px;
  }
  </style>
  </head>

  <body>

  <div class="cities">
  <h2>London</h2>
  <p>
  London is the capital city of England.
  it is the most populous city in the United Kingdom,
  with a metropolitan area of over 13 million inhabitants.
  </p>
  </div>
  
  </body>
  </html>

  //分类块级元素
    //HTML<div>元素是块级元素，它能够用作其他HTML元素的容器
    //设置<div>元素的类，使我们能够为相同的<div>元素设置相同的类
    //实例：
    <html>
  <head>
  <style>
  .cities{
    background-color:black;
    color:white;
    margin:20px;
    padding:20px;
  }
  </style>
  </head>

  <body>

  <div class="cities">
  <h2>London</h2>
  <p>
  London is the capital city of England.
  it is the most populous city in the United Kingdom,
  with a metropolitan area of over 13 million inhabitants.
  </p>
  </div>

  <div class="cities">
  <h2>Paris</h2>
  <p>Paris is the capital and most populous city of France</p>
  </div>
  
  </body>
  </html>

  //元素的行内元素
  //HTMl<span>元素是行内元素，能够用作文本的容器
  //设置<span>元素的类，能够为相同的<span>元素设置相同的样式
  //例：
  <html>
  <head>
  <style>
    span.red{color:red;}
  </style>
  </head>
  <body>

  <h1>My<span class="red">important</span>Heading</h1>

  </body>
  </html>
  //此处输出为：我的重要的(红色)标题

//HTML id 属性
  //HTML id 属性用于为HTML元素指定唯一的id
  //一个HTML文档中不能存在多个有相同id的元素

  //使用id元素
    //id属性指定HTML元素的唯一ID。id属性的值在HTML文档中必须是唯一的
    //id属性用于指向样式表中的特定样式声明。JavaScript也可以使用它来访问和操作拥有特定ID的元素
    //id的语法是：写一个#，后面跟一个id名称。然后，在花括号{}中定义CSS属性
    //以下例子中有一个<h1>元素，它指向id名称"myHeader"。这个<h1>元素将根据head部分中的#myHeader样式定义进行设置：
    <html>
    <head>
    <style
    #myHeader{
      background-color:lightblue;
      color:black;
      padding;40px;
      text-align:center;
      }
      </style>
      </head>
      <body>

      <h1 id="myHeader">My Header</h1>

      </body>
      </html>

      //Class与ID的差异
      //同一个类名可以由多个HTML元素使用，而一个id名称只能由页面中的一个HTML元素使用
      <style>
      /*设置id为“myHeader“的元素的样式*/
      #myHeader{
        background-color:lightblue;
        color:black;
        padding:40px;
        text-align:center;
      }

      /*设置类名为“city”的所有元素的样式
      .city{
        background-color:tomato;
        color:white;
        padding:10px;
      }
      </style>
      //注：一个是拥有为一id的元素，一个是一个类型里面的所有元素

      //通过ID和链接实现HTML书签
      //HTTML书签用于让读者跳转至网页的特定部分
      //如果页面很长，那么书签可能很有用
      //要使用书签，必须首先创建它，然后为它添加链接
      //然后，当单击链接时，页面将滚动到带有书签的位置
      //实例：
      //首先，用id属性创建书签：
      <h2>id="C4">第四章</h2>
      //然后，在同一张页面中，向这个书签添加一个链接(“跳转至1第四章”)
      <a href="#C4">跳转至第四章</a>
      //或者，在另一张页面中，添加指向这个书签的链接(“跳转至第四章”)
      <a href="html_demo.html#C4">Jump to Chapter 4</a>

      //在JavaScript中使用id属性
      //JavaScript也可以使用id属性为特定元素执行某些任务
      //JavaScript可以使用getElementById()方法访问拥有特定id的元素
      //实例：
      //使用id属性通过JavaScript来处理文本
        <script>
        function displayResult(){
          document.getElementByld("myHeader").innerHTML="Have a nice day!";
        }
        </script>

        //本章总结：
          //1.id属性用于为HTML元素指定的唯一id
          //2.属性的值在HTML文档中必须是唯一的
          //3.CSS和JavaScript可使用id属性来选取元素或设定元素样式
          //4.id属性的值区分大小写
          //5.id属性还可用于创建HTML书签
          //6.JavaScript可以使用getElementById()方法访问拥有特定id的元素

  //HTML Iframe
    //Iframe用于在网页内显示页面

    //添加iframe的语法
    <iframe src="URL"></iframe>
    //URL指向隔离页面的位置

    //Iframe-设置高度和宽度
    //hight和width属性用于规定iframe的高度和宽度
    //属性值的默认单位是像素，但也可以用百分比来设定(比如“80%”)
    //实例：
    <iframe src="demo_iframe.htm"width="200"height="200"></iframe>

    //Iframe-删除边框
    //frameborder属性规定是否显示iframe周围的边框
    //设置属性值为“0”就可以移除边框
    //实例：
    <iframe src="demo_iframe.htm"frameborder="0"></iframe>

    //使用iframe作为链接的目标
    //iframe可用作链接的目标
    //链接的target属性必须引用iframe的name属性
    //实例：
    <iframe src="demo_iframe.htm"name="iframe_a"></iframe>
    <p><a href="http;//www.w3school.com.cn">target="iframe_a"W3School.com.cn</a></p>

    //此笔记源自W3School教程
      
