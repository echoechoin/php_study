# HTML
Hyper text markup language
# 标记
### 元素
##### 标签  
双标签  
```html
<标签名></标签名>
```  
单标签  
```html
<标签名>
```
##### 属性  
```html
<标签名 属性="值"></标签名>
```
# 标记分类
### 主体标签
```html
<!DOCTYPE html>
<html>
<head>
	<title>lesson001</title>
	<meta charset="utf-8">
</head>
<body>
	
</body>
</html>
```
### 文本标签
```html
<!--加粗-->
<b>Bold</b>
<!--强调的加粗-->
<strong>Bold</strong>

<!--倾斜-->
<i>itatic</i>
<!--强调的倾斜>
<em>em</em>

<!--下划线-->
<u>underline</u>
<ins>ins</ins>

<!--删除线-->
<del>delete</del><br>
<s>s</s><br>

<!--字体
color
size:	1~7
face:	字体样式
-->
<font>font</font>

<!--字体变大15%-->
<big>big</big><br>
<!--字体变小15%-->
<small>small</small>

<!--上标-->
<sup>sup</sup>
<!--下标-->
<sub>sub</sub>
```

### 注释
```html
<!--There is comments.-->
```

### 排版标签
```html
<!--段落
段落标签上下有空隙
align: 	center/right/left
-->
<p>This is a paragraph.</p>

<!--换行标签-->
这里将会换行<br/>

<!--分割线
width:	
size:	
color:	
align:	center/right/left
noshade="noshade"
-->
<hr/>

<!--标题
align:	center/right/left
-->
<h1></h1>

<!--块标签
块标签独占一行
块元素可以设置宽高
-->
<div></div>

<!--行内标签
行内标签无法设置宽高
-->
<span></span>
```

### 列表标签
##### 有序列表
```html
<ol>
	<li>list1</li>
	<li>list2</li>
	<li>list3</li>
</ol>
```
有序列表的属性：
| attribules | values  |
| ------     | ------  | 
| type | 1/a/A/i/I/none|
| start | 起始位置(阿拉伯数字) | 
##### 无序列表
```html
	<ul>
		<li>list1</li>
		<li>list2</li>
		<li>list3</li>
	</ul>
```
无序列表的属性：  

| attribules |        values            |
| ------     |        ------            | 
| type       | disc(实心圆) square circ  |

### 图片标签
```html
<img src="https://cn.bing.com/sa/simg/SharedSpriteDesktop_2x_090619.png" />
```
img的属性：  

| attribules  |        values            |
| ------      |        ------            | 
| width/height|         \                |

### 链接标签
```html
<a href="https://www.baidu.com">baidu.com</a>
```

