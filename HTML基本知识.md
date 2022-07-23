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
-商标符号
&trade  ™
&reg  ®
