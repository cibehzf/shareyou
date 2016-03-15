### 前提

- `<html>`和`<body>`的高度设置为100%;
- 清楚默认样式, 即把margin和padding设置为0(如果不清除默认样式的话，浏览器就会出现滚动条)

如下:

	html, body {
            width: 100%;
            height: 100%;
            margin: 0;
            padding: 0;
        }

position方法:

	position: relative;
    top:50%;
    margin-top: -150px;/*元素自身高度的一半*/

flex方法:

	display: flex;
	align-items: center; /*定义body的元素垂直居中*/
	justify-content: center; /*定义body的里的元素水平居中*/