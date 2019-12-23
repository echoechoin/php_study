## 什么是css
层叠样式表 cascading style sheet，给页面上的标签添加样式。  
1998年W3C正式推出了CSS2，CSS2.1是W3C现在正在推荐使用的。  
使用css修改html样式而不是用html的属性。  

## 语法规则
格式声明语句要用`{属性：属性值}`括起来，里面放各种格式声明语句；  
在属性值的后面用`；`结束；  
CSS样式必须写单位（px等）；  

## CSS引入
#### 使用style属性引入(行内引入)：  
```html
<font style="color: red;">word</font>
```
#### 使用style标签引入（内嵌引入）：

```html
<!DOCTYPE html>
<html>
<head>
	<title>css test</title>
	<style type="text/css">
		div{
			color:yellow;
		}
	</style>
</head>
<body>
	<div>hello world!</div>
</body>
</html>
```

#### 外部引入
```html
<!DOCTYPE html>
<html>
<head>
	<title>css test</title>
	<link rel="stylesheet" type="text/css" href="lesson003.css">
</head>
<body>

</body>
</html>
```

## CSS核心语法
```html
选择器:{
	属性：值；<!-- 表示一个声明 -->
	属性：值；<!--表示另一个声明-->
}
```

## CSS选择器
### 基本选择器（简单选择器）

| \             | 含义                            |
| ---           | ---                             |
| `\*`           | 通用选择器，选择所有的标签        |
| `tagName`   | 标签选择器，选择指定的所有标签     |
| `.className`  | 类选择器，选择指定className的标签 |
| `#idName`     | id选择器,选择指定id的标签         |

伪类选择器（针对`<a>`和`<li>`标签）：  

| \         |    含义      |
| ---       | ---          |
| `a:link`    | 未访问过的    |
| `a:visited` | 访问过了的    |
| `a:hover`   | 鼠标放在上面的|
| `a:active`  | 鼠标点击过的  |


在使用伪类的时候，只能以上述的顺序写样式表。

### 复合选择器

|  \                   |   含义                                         |
|---                   | ---                                           |
| `选择器1,选择器2 ...` | 分组选择器，选择选择器1和选择器2选择的元素        |
| `选择器1 选择器2 ...` | 后代选择器，选择选择器1的后代并用选择器2选择的元素 |
| `选择器1>选择器2 ...` | 子代选择器，选择选择器1的子代并用选择器2选择的元素 |

### 选择器优先级

1. id选择器(权重：100)优先级高于class选择器(权重：10)，class选择器优先级高于tag选择器(权重：1)，tag选择器大于通用选择器(权重：0)。  
2. **如果是复合选择器，把权重相加得到的结果越大，优先级越高。**
3. 如果优先级相同，则后面的样式会覆盖前面的样式。

## css基础属性

### 尺寸
wdith：宽度  
height：高度  

### `元素转换`
display: block(转换为块元素) / inline(转换为行元素) / inline-block(函内块，即可设置宽高，也可以在同一行显示) / none(隐藏一个元素)。

### 字体
font: 设置font所有属性，应该有顺序：color font-style font-size font-weight font-style
font-size: 文字大小  
`font-famliy`: 字体  
`font-weight`：加粗(bold / normal)  
`font-style`: 倾斜(italic / normal)  

### 文本
color: 文本颜色  
`text-align`: center / left / right  
`test-decorator`: underline / overline / line-through /none  
`test-indent`: 首行缩进 *n*px / *n*em  
`letter-spacing`: 字间距  
`word-spacing`: 词间距  
`line-height`: 行高 【tips：让行高和高度相同就能使文字上下居中】  














