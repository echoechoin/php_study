# HTML
Hyper text markup language
# 标记
## 元素
### 标签  
双标签  
```html
<标签名></标签名>
```  
单标签  
```html
<标签名>
```
### 属性  
```html
<标签名 属性="值"></标签名>
```
# 标记分类
## 主体标签
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
## 文本标签
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

## 注释
```html
<!--There is comments.-->
```

## 排版标签
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

## 列表标签
### 有序列表 ordered list1
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

### 无序列表 unordered list
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

### 定义列表 define list

```html
<dl><!--定义列表标签-->
	<dt>列表名称</dt><!--定义标题标签-->
		<dd>列表定义</dd><!--定义说明标签>
	<dt>列表名称</dt>
		<dd>列表定义</dd>
</dl>
```

## 图片标签
```html
<img src="https://cn.bing.com/sa/simg/SharedSpriteDesktop_2x_090619.png" />
```
img的属性：  

| attribules  |        values            |
| ------      |        ------            | 
| width/height|         \                |

## 链接标签
### 网页链接
```html
<a href="https://www.baidu.com">baidu.com</a>
```
属性  
* target: \_self | \_blank | \_parent | \_top | framename

### 锚点
```html
<a name="dest">dest</a>
<a href="#dest">跳转到dest</a>
```

## 表格标签
```html
<table>
	<caption>表标题</caption>>=
	
	<thead><!--首行-->
		<th>列标题</th>
		<td>列标题</td>
	</thead>

	<tbody><!--主体-->
		<tr>
		<th>行标题</th>
		<td>单元格</td>
		</tr>
		<tr>
			<th>行标题</th>
			<td>单元格</td>
		</tr>
	</tbody>

	<tfoot><!--尾行-->
		...
	</tfoot>
</table>
```

`【注】`
* thead和tfoot应该只能出现一次，tbody可以出现多次；  
* 所有的没有明确归属到上述三个标签的行，都默认归属到tbody；  

table常用属性

| attributes   | values                                |
| ---          | ---                                   |
| border       | /                                     |
| `cellspacing`| 设置单元格与单元格边框之间的空白间距宽度 |
| `cellpadding`| 设置单元格与边框线之间的空白间距宽度 |
| width        |                                       | 
| height       |                                       |
| align        |                                       |
| bgcolor      |                                       |
| background   | 设置背景图                             |
| bordercolor  |                                       |

tr常用属性

| attributes   | values                                |
| ---          | ---                                   |
| align        |                                       |
| `valign`     | top / center / buttom                 |

td / th常用属性

| attributes   | values                                |
| ---          | ---                                   |
| width		   |                                       |
| height       |                                       |
| rowspan      | 上下合并 |
| colspan      | 左右合并 与excel不一样，合并了单元格后面的会向后移动，需要删除后面的单元格 |

##  表单标签

表单标签主要包括：form / input / select>option / textaera / button 
```html
<form action="脚本名字" method="get | post" name="form1">
	<legend>表单信息</legend>
	<fieldset>
		<!--表单项-->	
		ID:<input type="text" name="fname">
		<input type="submit" value="点击提交">
	</fieldset>
</form>
```
 form属性：  
* action: 提交目的地  
* method: 提交方法  
* name: 用于后端脚本区分获取的信息

### 单行文本框
```html
ID:<input type="text" name="fID" id="fID1" value="默认显示的内容">
<input type="submit" value="submit">
```
单行文本属性:  
* value: 默认显示的内容  
* size:长度
* maxlength: 最多能输入字符数
* readonly: 只读属性 
* disabled: 禁用  
* value: 默认值
* name: 控件名称
* id: 控件唯一标识符   

### 密码文本框
```html
<input type="password" name="fpasswd">
```

### 隐藏文本框
```hmtl
<input type="hidden" name="fhidden" value="传输不可见的内容">
```

### 单选项
```html
<input type="radio" name="fRadio" value="male" checked="checked">option1
<input type="radio" name="fRadio" value="female">option2
```

`【注】`
* 为了单选，必须把name设置为一样；
* value为传递的值
* checked表示默认选项

### 多选项
```html
<input type="checkbox" name="checkbox" value="option1">option1
<input type="checkbox" name="checkbox" value="option2">option2
<input type="checkbox" name="checkbox" value="option3">option3
```

`【注】`
* 一个多选项必须把name设置为一样；
* value为传递的值
* checked表示默认选项

### 文件域
```html
<input type="file" name="fFile">
```

### 按钮
```html
<!--文字按钮-->
<input type="submit" value="提交">

<!--图片按钮-->
<input type="image" src="url">

<!--重置按钮-->
<input type="reset" value="重置">

<!--普通按钮-->
<input type="button" value="普通按钮">
```

### 下拉列表
```hmtl
<select size="2" name="select">
	<option selected="selected" value="选项1">选项1</option>
	<option>选项2</option>
</select>
```

`【注】`
* seleted 表示默认选项  
* size 表示可以选择的个数  
* option的value表示传递的值，如果不写，则传递文本

### Optgroup选项组
```html
<selec name="char">
	<optgroup label="num">
		<option>1</option>
		<option>2</option>
	</optgroup>
	<optgroup label="letter">
		<option>a</option>
		<option>b</option>
	</optgroup>
</select>
```

### 文本域
```html
<textarea cols="10" rows="20" name="ftextarea"></textarea>
```

### 双标签按钮
```html
<button>提交</button>
```

### label
```html
<label for="id1">ID</label><input type="text" name="fId" id="id1">
```
* 在web点击ID就可以像点击input框后一样输入内容了

## 其他标签






## 标签关系
### 后代关系：包含关系、父子关系  
### 兄弟关系：同级关系，必须属于同父级的关系  

# html5标签
* html5与html4相比，有了巨大的进步。
* html5任然处于完善之中。然而大部分现代浏览器已经具备了某些HTML5支持
* `谨慎使用html5`

## 一些新增的标签

### 结构化语义标签。
article / aside / header / footer / nav / section / 等等。  
`这些标签主要是为了表示某种“含义”，但是其本身没有什么外观表现，根div一样。`

### 多媒体标签

```html
<audio>
	<source src="url/audio.mp3">
	<source src="url/audio.avi">
	不支持HTML5
</audio>
<video src="url/video.mp4">不支持HTML5</video>
```
多媒体标签属性：  
* src ： url
* autoplay : 是否自动播放。
`【注】`Google chrome不支持自动播放音频了,播放视频的时候需要添加mute属性。
* controls ： 是否显示播放控件 
* loop : 是否循环播放
* width : 宽度
* height : 高度

### 其他标签
* dialog: 对话框框【需要open属性】
* progress: 进度条。属性：value当前，max最大值
* mark: 重点标记
* time: 时间(语义化标签)
* address: 地址(语义化标签)
* canvas: 画布
* details / summary: 实现文本的展开和折叠
```html
<details>
	<summary>书籍</summary>
	书籍是人类进步的阶梯。
</details>
```

## 新增的input类型
* email
* tel
* url
* number: 属性：step步程
* search / datalist / option: 搜索框提示
```html
<input type="search" name="fsearch" list="d1">
	<datalist id="d1">
		<option>option1</option>
		<option>option2</option>
	</datalist>
```
* range: 滑块
* time
* date
* datetime
* month
* week
* color

## 新增的属性
### 在input中 
* required: 必填项
* placeholder: 文本提示内容
* autofocus: 自动获取焦点
* multiple: 设置文件域可以多选  

### 其他
* contenteditable: 设置一个元素可编辑


































