<link rel="stylesheet" href="http://yandex.st/highlightjs/6.1/styles/default.min.css">
<script src="http://yandex.st/highlightjs/6.1/highlight.min.js"></script>
<script>
    hljs.tabReplace = '    ';
    hljs.initHighlightingOnLoad();
</script>

## CSS3之2D变形

变形(transform)是指对html元素进行**位移(translate)**, **缩放(scale)**, **旋转(rotate)**, **倾斜(skew)**, **矩阵变形(matrix)**

### 位移translate

语法

- `translate(x, y);`向右为X轴正向, 向下为Y轴正向, x和y表示向x方向或者y方向移动的距离(用px或者%表示)

### 缩放scale

语法

- `scale(x);` 向水平方向和垂直方向缩放x倍
- `scale(x, y);` 向水平方向缩放x倍, 向垂直方向缩放y倍
- `scaleX(x);`只在水平方向缩放x倍
- `scaleY(y);`只在垂直方向缩放y倍

### 旋转rotate

- `rotate(a);`正值表示顺时针旋转, 负值表示逆时针旋转

### 倾斜skew

语法

- `skew(x, y);` 元素在水平和垂直方向上倾斜
- `skewX(x);` 元素在水平方向扭曲倾斜
- `skewY(y);` 元素在垂直方向倾斜

### 矩阵变形matrix

矩阵变形的可以实现镜像对称等复杂的2D变形, 这里需要一定的矩阵知识, 暂不做讨论.

### 元素的中心原点

对元素进行变形的时候, 通过改变元素的中心点, 让元素实现更加丰富的效果.

![](http://codropspz.tympanus.netdna-cdn.com/codrops/wp-content/uploads/2014/12/transform-origin-examples.png)

上图中同样旋转了45度, 却是以不同的原点进行旋转的

[代码在这里](http://tympanus.net/codrops-playground/SaraSoueidan/URYZ2oYI/editor)

语法

- `tranform-origin: x y;`

其中x, y的值可以是

- 像素
	- `transform-origin:100px 100px;`
- 百分号
	- `transform-origin:50% 50%`
- 具体位置
	- 用`top` `right` `bottom` `left` 组合指定
	- 例如`transform:top left;` 则表示元素原点在元素右上角的位置
	
		![](http://htmlbook.ru/files/images/css/css_transform-origin-1.png)







