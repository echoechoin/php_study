# CSS Box
盒子就是一个元素（标签）的所辖范围，简单来说，基本就是一个“矩形区域”。

## 盒子概述
一个盒子的构成：`content padding border margin`。  

### 盒子的宽度和高度
* 设置盒子的width和heigh实际上设置的是盒子的content的宽高。  
* 总高(宽)度 = margin + border + padding + width(height)。  
* 行内元素不可以设置宽高
```html
<style type="text/css">
	div{
		width: 100%;
		min-width: 50%；
		max-width: 100%;
		min-height: 50%;
		max-height: 100%;
	}
</style>
```

### border 边框
```html
<style type="text/css">
	div{
		// 三个常用属性
		border-style: solid | dashed | dotted;
		border-width: 1px;
		border-color: #000000;

		border: ;
		border-top: 1px solid black;// 没有顺序
		border-bottom: 1px solid black;
		border-left: 1px solid black;
		border-right: 1px solid black;
	}
</style>
```

### padding 内边距
```html
<style type="text/css">
	*{
		padding: 0;
	}
	div{
		padding-bottom: 1px;
		padding-left: 1px;
		padding-right: 1px;
		padding-top: 1px;
		
		padding: 1px 2px 3px 4px; // 上 右 下 左
		padding: 1px 2px 3px // 上 左和右 下
		padding: 1px 2px // 上和下 左和右
		padding: 1px; // 上下左右
	}
</style>
```
* `【注】padding不支持负数，而margin支持`

### margin 外边距
```html
<style type="text/css">
	*{
		padding：0；
		margin: 0;
	}
	div{
		margin-top: 1px;
		margin-bottom: 1px;
		margin-left: 1px;
		margin-right: 1px;

		margin: 1px 1px 1px 1px; // 上 右 下 左
		margin: 1px 1px 1px; // 上 左和右 下
		margin: 1px 1px; // 上和下 左和右
		margin: 1px; // 上下左右
	}
</style>
```
 `***【注】两个盒子的上下margin会重叠，以最大margin为准***`  
 `***【注】一个主盒子的子盒子上下margin与外面的另一个盒子的上下margin也会发生重叠***`  
解决方法：给主盒子添加样式：overflow: hidden; | 给主盒子添加边框 | 给主盒子添加padding  

* `盒子在父盒子中居中的方法`：
```html
<style type="text/css">
 div{
		width: 960px;
		margin: 0 auto; // 盒子的居中方法
 }
</style>
```

### background 背景
```html
<style type="text/css">
	div{
		background-color: black; // 背景颜色
		background-image: url(./sample.jpg); // 背景图片
		background-repeat: repeat | repeat-x | repeat-y | no-repeat // 背景是否重复
		background: url(./sample) no-repeat // 统一设置的方法

		background-position: 10px 10px; // 修改背景图片的位置
		background-position: 30% 30%;
		background-position: left|center|right buttom|center|top;

		/* 设置多个背景图片 */
		background: url(./sample.jpg)  no-repeat left  buttom,
					url(./sample2.jpg) no-repeat right buttom;
	}
</style>
```

### outline 轮廓
```html
<style type="text/css">
	div{
		outline-width: 1px;
		outline-style: dashed | dotted | solid;
		outline-color: red;
		outline-offset: 1px; // 轮廓线与边框线之间的距离
	}
</style>
```
`【注】轮廓线不影响页面的排版`  




# 布局

## 标准文档流排版
* 没有任何CSS样式的排版，一个块元素占据一行，多个行内元素可以在一行。
  
## display 排版
```html
<style type="text/css">
	div | span{
		display: block | inline-block | inline | none;  
	}
</style>
```
* block 块元素  
* inline 行内元素 `行内元素上下边框不占用空间，左右边框占用空间`。  
* inline-block 行内块元素 `行内块元素在一行的时候，两两有一点空隙`。
* none `不显示元素` 且 不占用页面布局   

## overflow 溢出

* 一个盒子内部的内容，超出了该盒子的设定大小的时候，由overflow样式决定怎么显示该内容。  
```html
<style type="text/css">
	div{
		overflow: auto | hidden | scroll | visible; 
	}
</style>
```
* auto 依照浏览器
* hidden 隐藏溢出的内容
* scroll 滚动条
* visible 可见

## visibility 可见性
* 该样式设置为hidden和display设置为none的区别就是隐藏了也会占用空间而display设置了不占用空间。  
```html
<style type="text/css">
	div{
		visibility: hidden | visible;
	}
</style>
```

## float 浮动

* 让一个元素往左或往右“尽量挤靠”，以使周边`行内元素`或`文字`可以围绕该浮动元素显示。类似word的图片浮动。  
* 让一个`块元素`脱离标准文档流。  

```html
<style type="text/css">
	div{
		float: left | right | none;
	}
</style> 
```

* `【注】默认情况下浮动元素的父元素无法包含浮动元素。`
* 清除浮动的方法：
方法一: 给浮动元素的父元素添加样式overflow: hidden;   
方法二: 在浮动盒子的父元素里添加一个块元素，该块元素设置clear: left | right | both;  
方法三: 给浮动元素的父元素添加height。
`方法四(推荐)`: 在浮动盒子的父元素的里添加一个伪元素：

```html
<style type="text/css">
	div::after{
		content: "";
		display: block;
		clear: both;
	}
</style>
```

## position 定位
* 通过有关定位的属性来明确设定一个盒子在平面(x,y)上所处的位置和在高度(z)上所处的位置。  
* `【注】`absolute和fixed脱离了文档流。 

### static 静态定位
以标准文档流定位。  

### relative 相对位置
* 以原来位置为基准，需要设定top left right bottom。
* 相对定位会占有原文档的位置。

### absolute 绝对位置
* `相对其上层最近的一个非static定位元素而设定的一个绝对性定位`，需要设定top left right bottom；
* 如果其祖先都没有定位，默认以`body`定位。 
* 绝对定位不会占有原位置的空间。

### fixed 固定位置
* 相对于当前网页窗口的一个绝对定位定位；  
* 固定定位不会占有原位置的空间。

### z-index 层级
* 当 相对定位 绝对定位 固定定位 时，默认的层级就是谁的HTML文档在下面谁的文档层级显示在外面。 
* z-index取整范围： -99 ~ 99，数字越大，层级越靠上；




# 列表与表格样式

## list 列表
* 无序列表和有序列表在CCS中没有本质区别。
```html
<style type="text/css">
	ul ol{
		list-style-type: ; // 列表样式类型
		list-style-image: url(img.jpg); // 图片取代列表样式类型
		list-style-position: outside | inside; // 列表索引的位置
	}
</style>
```
* 在实际应用中，一般使用背景图取代list-style-image和list-style-type。

## table 表格
```html
<style type="text/css">
	table{
		border-collapse: separate | collapse; // 设置表格的单元格边线是否合并
		border-spacing: 1px; // 设置表格单元格之间的间隙大小（只有在border-collapse: separate;时才有效）
		caption-side: bottom | left | right | top; // 设置表格标题的位置
	}
</style>
```

















