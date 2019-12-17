## 什么是css
层叠样式表 cascading style sheet，给页面上的标签添加样式。  
1998年W3C正式推出了CSS2，CSS2.1是W3C现在正在推荐使用的。  

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

| 符号   | 含义      |
| ---   | ---       |
|  `*`  | 通用选择器，选择所有的标签 |
|  `标签名`| 标签选择器，选择指定的所有标签 |
|  |  |

### 复合选择器




