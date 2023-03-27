# 媒体查询(硬件查询)

> 通过设备的不同自动加载不同的样式. (通过vscode生成初始html自带的<meta>标签)

```html
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
    @media screen and (max-width: 768px){
        a
    }
</style>
</head>
```

# 雪碧图(css Sprite)

> 一次请求将一批属性相同的图片转为一张图发送给客户.

1. 通过`background-image`引入图片
2. 通过`background-position`将图片移动到所需的位置


