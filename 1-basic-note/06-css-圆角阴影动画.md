# 圆角与阴影
#web/css

## 圆角边距
```css
boder-redius: length; /*10px,50%/
```
> 后面可以跟4个值,分别表示 左上,右上,右下,左下
> 后面可以跟2个值,分别表示 (石上,左下)

## 盒子阴影
```css
.showbox:hover {
 	box-shadow: 0px 10px 10px -5px rgba(0, 0, 0, 0.3);
 }
```

> box-shadow: h-shadow, v-shadow, blur, spread, color, inset

| 值       | 描述                            |
| -------- | ------------------------------- |
| h-shadow | 必须,水平阴影位置,可以为负值    |
| v-shadow | 必须,垂直阴影位置,可以为负值    |
| blur     | 可选,模糊距离                   |
| spread   | 可选,影音尺寸                   |
| color    | 可选,阴影颜色                   |
| inset    | 可选,将外部阴影(outset)改为内部 |

## 文字阴影

```css
test-shadow: h-shadow, v-shadow, blur, colo
```

## 动画

- 动画是使元素从一种样式逐渐变化为另一种样式的效果.
- 可以改变任意多的样式任意多的次数.
- 请用百分比来规定变化发生的时间，或用关键词from和"to"等同于0%和100%
- 0%是动画的开始，100%是动画的完成

### 创建

使用`@keyframe`创建动画
```html
@keyframe first-animi {
	from{
		background-color: red;
	}
	20% {
		background-color: blue;
	}
	100% {
		background-color: black;
	}
}

```
### 使用

> animation: name duration timing-function delay iteration-count direction;

```html
.box {
	height: 100px;
	width: 100px;
	background-color: #fff;
	animation: my-animi 2s linear 0s infinite alternate;
}
.box:hover{
	animation-play-state: paused;
}
```
