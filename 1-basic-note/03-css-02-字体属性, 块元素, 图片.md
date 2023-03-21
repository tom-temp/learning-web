# 2-CSS-02

#web/css

- [字体属性](#字体属性)
	- [字体复合属性](#字体复合属性)
    - [文本属性](#文本属性)
- [转化为块元素](#转化为块元素)
- [背景图片](#背景图片)

---

## 字体属性

```html
<style>
	body {
		font-family: Arial, 'Microsoft YaHei';
		font-size: 20px;
		font-weight: normal; <!-- normal| bold| bolder| lighter| 某个数字-->
		font-style: normal;<!--italic-->
	}
</style>
```

> 一般情况下，网页中不会有倾斜字体，所有常把`<em>`标签与`<i>`标签的字体设为正常字体.
> chrome浏览器能显示的最小字体是12px

```html
<style>
	em {
		font-style: normal;<!--italic-->
	}
</style>

<em>字体变为正常字体</em>
```

### 字体复合属性

`font: font-style font-weight font-size/line-hight font-family;`

==font-size==与==font-family==为必须属性,必须要写

```html
<style>
	body {
		font: italic 600 16px 'Microsoft YaHei';
	}
</style>
```

### 文本属性

> 文本显示的模式

```html
<style>
	body {
		color: red;

		<!--水平对齐方式: left/right -->
		text-align: center;
		vertical-align: center;

		<!-- 文字增加线: none/underline/overline/line-through -->
		text-decoration: underline;

		<!-- captialize 首字母大写 -->
		<!-- uppercase  全大写 -->
		<!-- lowercase  全小写 -->
		text-transform: captialize;

		<!-- 首行缩进,可以为负数,2em为当前元素2个文字的大小 -->
		text-indent: 2em;

		<!-- 此选项由"上间距+文字高度+下间距"三者构成 -->
		line-height: 26px;
	}
</style>
```


---

## 转化为块元素
```html
<style>
    a {
		display: block;<!-- inline/inline-block -->
        width: 160px;
		height: 500px;
		color: black;
        text-decoration: none;
		background-color: pink;
    }
	a:hover {
        color: blue;
        text-decoration: underline;
    }
```

##  背景图片

```html
<style>
	div {
		background-color: red;
		background-image: url(); <!--必须带有url(),本地连接也在url里写-->
		background-repeat: repeat; <!--重复显示方式 no-repeat/repeat-x/repeat-y -->

		<!-- cover contain 会保持图片纵横比 -->
		background-size: 100% auto; <!-- 数字-宽高/百分比-宽高/'cover'/'contain'   -->

		<!-- 图片出现的位置 -->
		background-position: center top;
		background-position: 20px 50px; <!--x坐标, y坐标 -->
		background-attachment: scroll; <!--图片是否滚动 scroll/sixed-->

		background: color url() repeat scroll 20px top;
	}
</style>
```
