# 脱离文档流

> 一般而言, 块元素从上到下, 行内联元素从左到右.

- 普通文档流默认
  - 下方对齐
  - 图片有缝隙

- 三种方法脱离文档流
  - 浮动
  - 绝对定位
  -固定定位

## 浮动

> 增加一个浮动层, 使元素向左或向右浮动

```html
.box1 {
    float: left | right;
}

```

### 清除浮动

> 元素浮动会使父元素的高度塌陷,
> 后续元素也会受到影响

1. 父元素设置高度
2. 受影响的元素增加`clear`属性
3. 父元素增加overflow清除浮动
4. 父级元素伪对象方式


> 2. 受影响的元素增加`clear`属性
```html
.box2 {
    clear: both;
}
```
> 3. 父元素增加overflow清除浮动
```html
.box-container {
    overflow: hidden;
    clear: both;
}
```
> 4. 父级元素伪对象方式
```html
.box-container::after {
    content: "",
    display: block;
    clear: both;
}
```

## 定位

```html
.box {
    position: relative | absolute | fixed
}
```
> absolute(绝对定位), fixed(固定定位)会脱离文档流


### 相对与绝对定位

> 相对与绝对定位的元素位置的锚点是**有定位(position)属性的父级元素**.
> 一般来说, 在开发中, 父级属性为`position: relative;`, 子级属性为`position: absolute;`

```html
.box-re {
    position: relative;
    left: 100px;
    top:  100px;
}

<!-- 每一个绝对定位都是一层 -->
.box-ab {
    position: absolute;
    left: 100px;
    top:  100px;
}
```

## z-index

> 调整绝对定位产生图层的顺序, 越大,图层越考上


```html
.box-1 {
    position: absolute;
    left: 50px;
    top:  50px;
    height: 100px;
    width:  100px;
    z-index; 100;
    background-color: red;
}

<!-- 每一个绝对定位都是一层 -->
.box-2 {
    position: absolute;
    left: 100px;
    top:  100px;
    height: 100px;
    width:  100px;
    z-index: 90;
    background-color: green;
}
```
