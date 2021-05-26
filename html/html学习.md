- 标签书写注意规范
  ```
  基本语法概述
  html标签必须是由尖括号包围的关键字，eg：<html>
  大部分情况下，html标签是成对出现的例如<html></html>, 称为双标签，开始标签-结束标签。
  有些特殊的标签必须是单个标签，极少情况下。如<br/>, 称为单标签。
  标签具有两种关系：父子关系和兄弟关系
  ```
- html 骨架标签
  ```
  每个页面都会有一个基本的结构标签，也称为骨架标签。页面标签在这些基本标签之上书写，html页面也称为html文档.
  浏览器的作用就是读取html文档，然后以网页的形式展示出来
  <html>
    <head>
        <title>第一个页面</title>
    </head>
    <body>
        文件
    </body>
  </html>
  ```

- vscode插件安装
  ```
  chinese 汉化
  open in browser 方便调试
  auto rename tag 自动重命名配对的标签
  ```


- html解释
  ```
  <!DOCTYPE html>   文档类型(版本)声明。这个表示当前页面使用html5来显示
  <html lang="en">   当前文档的显示语言，zh-CN中文
  <head>
    <meta charset="UTF-8">  声明字符集，万国码
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>创建第一个页面</title>
        
  </head>
  <body>
        写代码是一件非常快乐的事情
  </body>
  </html>

  ```

- 常用标签
  ```
  标题标签<h1>-<h6>, 作为标题使用，重要性递减
  段落标签<p></p> 文本在浏览器中会根据浏览器的大小自动换行 段落之前保有空隙
  强制换行<br />，单个标签，简单另起一行
  文本格式化标签 
  <strong></strong><b></b>加粗
  <em></em><i></i>  斜体
  <del></del><s></s> 删除线
  <ins></ins><u></u> 下划线
  布局：
  <div></div>  没有语意用来创建布局 一行只能有一个div，大盒子
  <span></span> 没有语意用来创建布局 一行可以放多个span
  图像标签：
  <img src="图像url"/>， 单标签，src是必须属性，用于指定文件路径和文件名
    <img src="test.png" alt="图像显示不出来提示文字" title="提示文字" width="200" height="500" border="15">

  超链接标签：
  <a href="http://www.baidu.com" target="_blank"> haha</a>   
  <a href="http://www.baidu.com" target="_self">  haha</a>  
  target="_blank" 打开新窗口
  target="_self"  在当前窗口打开

  外部链接和内部链接：
  外部链接链接到外网，内部链接，链接到网站内部
  内部链接
  <a href="index.html" target="_blank"> haha</a>
  空链接
  <a href="#" target="_self"> haha</a>
  下载链接
  <a href="a.zip" target="_blank"> 下载</a>

  网页中各种元素都可以添加超链接（）

  锚点链接：点击链接快速定位到页面别的位置, 通过标签的id进行定位
  <a href="#live2" target="_blank"> 下载</a>
  <h1> id= "live">yfkfkfykfkyfk</h1>
  
  注释标签：
    <!-- 注释标签： --> ctrl+/

  特殊字符：
    &nbsp;  空格 
    &lt;    小于号 
    &gt;    大于号

  表格标签：
    表格不是用来布局页面的而是用来展示数据的。
        <table>   // 表格标签
        <tr>      // 行
            <td>姓名</td> //单元格，不是列
            <td>性别</td>
        </tr>
        <tr>
            <td>刘德华</td>
            <td>张学友</td>
        </tr>
    </table>
    表头单元格标签（加粗居中显示）：
        <table>
        <tr>
            <th>姓名</th>  // 表头单元格
            <th>性别</th>
        </tr>
        <tr>
            <td>2</td>
            <td>2</td>
        </tr>
    </table>
    表格属性（不常用，一般使用css进行控制）：
        对齐     <table align="center">
        边框     border="1"
        文字距单元格距离    cellpadding="20"
        单元格之间距离   cellspacing="0"（边框无空隙）
        高和宽：   width="1000" height="2000"
    表格结构标签（主要作用是让代码有更好的语义）
         <thead>表头区域</thead>
         <tbody>身体区域</tbody>   
    合并单元格：
          语法：
            rowspan="合并单元格的个数"，跨行合并
            colspan="合并单元格的个数"，跨列合并
          跨行写到最上侧，跨列写到最左侧  
  列表标签：
        列表用来布局的。整齐，整洁，有序。
        分为，
        无序列表（重点），ul标签内只能放li标签，li标签内可以容纳所有元素，有自己的样式属性，实际使用时，可以通过css来设置
            <ul>
               <li>列表1</li>
               <li>列表2</li> 
               <li>列表3</li>
            </ul>
        有序列表   ol标签内只能放li标签，li标签内可以容纳所有元素，有自己的样式属性，实际使用时，可以通过css来设置
              <ol>
                <li>列表1</li>
                <li>列表2</li>
                <li>列表3</li>
              </ol>
        自定义列表（重点） dl标签里只能包含dt和dd，dt和dd个数没有限制，经常是一个dt对应多个dd
                <dl>
                  <dt>名词</dt>
                  <dd>名词解释</dd>
                  <dd>名词解释</dd>
                </dl>
  表单标签：
        作用：收集用户信息
        组成：表单域、表单控件（表单元素）、提示信息三部分构成
        表单域： 主要作用是将范围内的表单元素信息提交给服务器
            <form action="url地址" method="提交方式" name="表单域名称">各种表单元素控件</form>
        表单元素：
        input：
    <form action="url地址" method="提交方式" name="表单域名称">
        <!-- 文本 --> 
        <!-- name是表单元素名字，单选和复选按钮元素都必须有相同的name值 value是表单元素的值，这两个主要用于后台 -->
        <!-- 单选和复选框，可以设置默认选择 checked -->
         <!-- maxlength规定输入字段中字符的最大长度 -->
        用户名: <input type="text" name="username" value="" maxlength=6>    <br>
        <!-- 密码 -->
        密码: <input type="password" name="password" value=""> <br>
        <!-- 单选  这里表单元素名字必须相同才能实现单选效果-->
        性别: 男 <input type="radio" name="sex" checked="checked"> 女 <input type="radio" name="sex"> <br>
        <!-- 复选 -->
        爱好： 打篮球 <input type="checkbox"> 羽毛球  <input type="checkbox"> 乒乓球  <input type="checkbox"> <br>
        <!-- 提交按钮 通过value修改提交的name， 通过用户点击这个来提交表单元素到后台服务-->
        <input type="submit" value="免费注册">  <br>
        <!-- reset重置表单数据，还原 -->
        <input type="reset" value="重新填写">  <br>
        <!-- 普通按钮button 后期结合js搭配使用 -->
        <input type="button" value="获取短信验证码"> <br>
        <!-- file 提供文件上传 -->
        上传文件 <input type="file"> <br>
        <!-- label标签 为input元素定义标注，绑定一个表单元素，当点击label标签内的文本时，浏览器会自动选择对应的表单元素，增加用户体验 -->
        <!-- label中的for属性应该于input中的id相同 -->
        <label for="sex">男</label>
        <input type="radio" name="sex" id="sex">
    </form>
        select：多个选项让用户选择，并且想要节约页面空间，可以使用select定义下拉列表
          <form action="url地址" method="提交方式" name="表单域名称">
        <!-- select option实现下拉列表，select下至少包含一个option option中定义selected="selected" 实现默认值-->
        籍贯：<select name="" id="">
            <option selected="selected">山东</option>
            <option value="">北京</option>
            <option value="">天津</option>
        </select>
    </form>
        文本域： 当用户输入内容较多的时候，我们不能使用文本框表单了，使用textarea标签，常用于留言板、评论 

  综合案例（注册页面）：
      注册页面
  查阅文档： 
      w3school
      mdn      
  ```
