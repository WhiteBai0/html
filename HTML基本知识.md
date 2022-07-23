#html基本知识
---
##常用标签
* 标题标签h1到h6越来越小
```html
<h1><h1/>
<h2><h2/>
<h3><h3/>
<h4><h4/>
<h5><h5/>
<h6><h6/>
```
* 文本标签
```html
<p>段落文本内容</p>
<!-- 表示一个段落 -->
```
* 换行标签
```html
<br/>
<!-- 换行是一个强制空标 -->
```
* 水平线
```html
<hr/>
<!-- 空标记 -->
有四个属性颜色color,宽度width,对齐方式align,取消阴影noshade
```
**注意事项:换行是强制换行，和p标签不同的是连续两个p标签中间会有一个空行，br没有**
* 加粗有两个标记
```html
<b>加粗内容</b>只是显示加粗
<strong>强调的内容</strong>突出的文本
<!-- 推荐使用strong -->
```
* 倾斜有两个标记
```html
<em>强调文本</em>
<i>倾斜文本</i>
```
* 删除有两个标记
```html
<s>文本</s>删除线
<i>文本</i>删除线
```
- div标签
```html
<div></div>划分一个区域，没有具体含义，一个标签占满一行
```
- span标签
```html
<span></span>
没有具体含义，如果有一段文本内容，需要给其中部分进行独立修饰
```
- 列表标签
```html
1.有序列表：
<ol>
    <li></li>
    <li></li>
</ol>
ol当中只能放li，数字是自动生成的
其中ol标签当中有两个属性type：1,a,A,i,I;    start:只能是是一个数字，且满足该type下的进制，如type="a" start="27"，得到的有序序号将会是aa开始

2.无序列表：
<ul>
    <li></li>
    <li></li>
</ul>
ul当中只能放li，默认是黑色的实心圆
其中type属性有三个分别是：disc(默认)，circle(空心圆圈)，square(正方形)，none(没有任何)

3.自定义列表：
<dl>
    <dt></dt>
    <dd></dd>
</dl>
```
- 图片标签
```html
<img src="图片路径" title="鼠标悬停上去的提示信息" alt="图片加载失败的提示信息" width="" height=""/>其中src是必须，如果宽度和高度任选其一，则图片将会自动按原比例缩放
```
- 超链接标签
```html
<a href="路径" title="鼠标悬停上去的提示信息" target="规定在何处打开文档">内容</a>
target="_self"默认值，在当前窗口打开
target="_blank"在新窗口打开
```
- 表格标签
```html
<table border="外边框大小" width="表的宽度" height="表的高度 " align="表格的位置" bordercolor="表格颜色" bgcolor="背景颜色" cellspacing="单元格之间的间距" cellpadding="单元格和内容的空隙">
    <tr height="每一行的高度" bgcolor="每一行背景颜色" align="文字水平对齐" valign="文字垂直对齐top/middle/bottom">
        <td width="一列的宽度受到变化" height="一行的高度收到变化" align="该单元格文字水平对齐" valign="该单元格文字垂直对齐" bgcolor="每一单元格背景颜色"></td>
    </tr>
    <!-- 表示第一行有一个单元格 -->
    <tr>
        <td colspan="竖直合并单元格跨度"></td>
        <td rowspan="横向合并单元格跨度"></td>
    <!-- 表示第二行有两个单元格 -->
    </tr>
</table>
```
- 表单标签
```html
<form method="get或者post" action="向何处发送表单数据">
    <input/>
        A.属性type定义输入框的类型
            a)文本框type="text" 密码框type="password"
            b)提交框type="submit"和<button>提交按钮</button>一样
            c)按钮框type="button"单纯的按钮
            d)重置框type="reset"清空的效果
        B.属性placeholder描述输入字段预期值的简短的提示信息。兼容到E8以上
        C.属性name必须设置，否则在提交表单时，用户在其中输入的数据不会发送给服务器(显示在网址当中的内容)
        D.属性value是显示在button按钮上面的内容
</form>
```
* 其他
```html
<u>文本</u>下划线
<sub></sub>下标
<sup></sup>上标
```
## html特殊符号输入输出问题
- 尖角符号
&lt &gt
分别是<和>
- 空格符号
&nbsp受字体占据宽度影响，不推荐使用
&emsp始终都是占用一个中文字符的宽度
- 版权符号
&copy  ©
- 商标符号
&trade  ™
&reg  ®
## html中加入css文件内容
#### (优先级满足就近原则：外部样式表<内部样式表<行内样式表)
1. 内部样式表
```html
以h1标签为例
<style>
    h1{
        color:red
    }
</style>
```
2. 外部样式表
```html
当你写好一个css文件后可以通过link标签将css文件导入到html文件当中，同时导入的代码一般放在head标签当中
<link rel="stylesheet" type="text/css" href="css文件的路径">
或者
<style>@import url(文件路径)</style>
```
3. 行内样式表
将style作为一个属性，可以加到每一个标签当中
```html
<div style="color red">123456</div>
```
## 选择器
- 类选择器
  - 语法
  .类名{属性：属性值}
  - 说明
  A)当我们使用class选择符时，应先为每个元素定义一个class名称
  B)class选择符的语法格式如下
  ```html
  <style>
      .top{width:200px;height:100px;background:green}
  </style>
  <div class="top"></div>
  ```
  注意事项：当一个class中标识了多个类时，按照style中的顺序，后面的将会覆盖前面的
- id选择器
  - 语法
   #id(属性：属性值)
  - 说明
  A)当我们使用id选择符时，应该为每一个元素定义一个id属性
  如：
  ```html
  <div id="box"></div>
  ```
  B)id选择符的语法格式是"#"加上自定义的id名称
  如：#box{width:300px;height:300px}
  C)起名时要取英文名，不能用关键字：(所有的标记和属性都是关键字)
  如:head标记
  D)一个id名称只能对应文档中一个具体的元素对象。(唯一性)
- 通配符选择器
  - 语法
  *{属性:属性值}
  - 说明：含义是所有元素
```html
*{margin:0;padding:0}
<!-- 代表所有所有元素清除默认边距值和填充值 -->
```
- 群组选择器
  - 说明
  提供公共代码，节省代码量，和类选择器不同的是，它可以将一整个类进行修改
  - 示例如下
```html
<style>
    div,.box,h1{
        background-color:yellow
    }
</style>
```
- 后代选择器
  - 说明
  找到指定标签进行修改
  - 示例如下
```html
<style>
  div p{background-color:red}
</style>
<!-- 对所有div标签下的p标签进行修改 -->
```
- 伪类选择器
 - 语法
a:link{属性：属性值}超链接的初始状态
a:visited{属性：属性值}超链接被访问后的状态
a:hover{属性:属性值}鼠标悬停，即鼠标划过超链接时的状态
a:active{属性：属性值}超链接被激活时的状态，即鼠标按下超链接的状态
**注意：**：务必要按照顺序写入link->visit->hover->active
 - 示例
```html
<style>
    a:link{color:red}
</style>
```