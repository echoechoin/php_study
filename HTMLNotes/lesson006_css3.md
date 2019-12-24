# css3高级特性
* 盒子新特性
* 多栏布局
* 弹性布局
* 2D变换
* 3D变换
* 过渡属性
* 动画属性

## 盒子新特性

### 盒子阴影
```html
<style type="text/css">
	div{
		border: 1px solid red;
		box-shadow: 水平偏移值 垂直偏移值 [模糊值] [外延值] [颜色] [inset];
	}
</style>
```
* 至少设置两个长度值，分别表示阴影的水平偏移量和垂直偏移量，可以为负；
* 模糊值是设定阴影的模糊效果的宽度；
* 外延值是设定阴影再“扩大”的宽度；
* inset表示设置内阴影，默认是外阴影。

### 边框圆角
```html
<style type="text/css">
	div{
		border-radius: [水平]/[垂直]
		border-radius: 1px/3px; // 四个角
		border-radius: 1px 1px; // 上左下右 上右下左
		border-radius: 1px 1px 1px 1px; // 上左 上右 下右 下左
	}
</style>
```
* 实例：圆形头像
```html
<!DOCTYPE html>
<html>
<head>
	<title>圆形头像</title>
	<style type="text/css">
		#pic{
			width: 100px;
			height: 100px;
			border-radius: 50px;
			overflow: hidden; 
		}
		#pic img{
			width: 100px;
		}
	</style>
</head>
<body>
	<div id="pic">
		<img src="./sample.jpg">
	</div>
</body>
</html>
```

### 图像边框
```html
<style type="text/css">
	div{
		border: 10px solid; // 有的浏览器需要border属性！

		border-image-source: url(./sample.jpg);
		border-image-slice: 1; // 四个方向切割一样的值
		border-image-slice: 1 2; // 上下 左右
		border-image-slice: 1 2 3; 
		border-image-slice: 1 2 3 4 [fill]; // 不可以带单位,fill表示中间的填充

		border-image-width: auto; // 表示和slice的宽度一样

		border-image-repeat: repeat; // 是否以重复的方式填充边框和背景（默认是拉伸: stretch最常见）
		border-image-repeat: round; // 调整来刚好放置整数个数
		border-image-repeat: space; // 拉伸空格

	}
</style>
```

### 背景图滚动特性
```html
<style type="text/css">
	div{
		background-attachment: fixed | scroll | local;
	}
</style>
```
* fixed: 相对于当前浏览器固定;
* scroll: 相对于当前盒子固定（默认值,最常见）;
* local: 相对于内容固定（跟着内容动）

### 背景图原点设定
```html
<style type="text/css">
	div{
		background-origin: border-box | content-box | padding-box;
	}
</style>
```

### 背景图裁剪
```html
<style type="text/css">
	div{
		// 设置裁切区域   只在border以内出现 只在内容区出现  只在padding以内出现
		background-clip: border-box     |  content-box   |    padding-box;
	}
</style>
```

### 背景大小
```html
<style type="text/css">
	div{ //              指定大小     自动缩放覆盖到整个盒子 不会重复  自动缩放到刚好能被盒子包含 会重复 
		background-size: 100px 100px |             cover          |             contain;
	}
</style>
```

### 多背景
```html
<style type="text/css">
	div{
		background: 第一个背景图设置, 第二个背景图设置, ... [,背景颜色];
		// 背景源 背景位置[/背景大小] 背景重复 背景滚动性 ... ,
	}
</style>
```
### 背景图渐变色
* 线性渐变
```html
<style type="text/css">
	div{
		background-image: liner-gradient([角度，默认180deg] 颜色1, 颜色2, ...[,颜色n]);
		background-image: liner-gradient(90deg, red, blue, green);

		background-image: liner-gradient(0deg, red, blue 30px, green);

		background-image: liner-gradient(0deg, red, blue 20%, green 30%);
	
		background-image: liner-gradient(0deg, red, blue, green);	
	}  
</style>
```
* 镜像渐变
```html
<style type="text/css">
	div{
		// 我佛了 有用到再查
	}
</style>
```

## 多栏布局
* 类似word的多栏布局。
```html
<style type="text/css">
	div{
		/* 栏数与栏宽并没有什么关系，下述属性只需要设置一个 */
		column-width: ; // 栏宽属性
		column-count: ; // 栏数量
		column: 栏宽 栏数;

		column-gap: ; // 栏间隙
		column-rule: ; // 栏分割线
		column-rule-style: ;
		column-rule-width: ;
		column-rule-color: ;
	}
</style>
```

## 弹性布局








