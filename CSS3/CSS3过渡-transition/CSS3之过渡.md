<link 
="stylesheet" href="http://yandex.st/highlightjs/6.1/styles/default.min.css">
<script src="http://yandex.st/highlightjs/6.1/highlight.min.js"></script>
<script>
    hljs.tabReplace = '    ';
    hljs.initHighlightingOnLoad();
</script>

### CSS3过渡使用入门

在CSS中创建简单的过渡效果可以从以下几个步骤来实现：

1. 在默认样式中声明元素的初始状态样式；

		.demo{
			width:20px;
		}

2. 声明过渡元素最终状态样式，例如通过hover触发是的width变大

		.demo{
			width: 20px;
			transition: width 1s linear 0.5s;
		}	
		.demo:hover{
			width: 100px
		}

3. 在默认样式中通过添加过渡函数，添加一些不同的样式。
		
		.demo{
			width: 20px;
			transition: width 1s linear 0.5s;// 过渡函数
			// width代表要进行过渡的属性
	        // 1s代表过渡持续的时间
            // linear代表过渡的动画效果
            // 0.5s代表的是事件触发到开始过渡的时间
		}	
		.demo:hover{
			width: 20p;
		}
		
通过以上三步, 就可以实现当鼠标悬浮在`.demo`元素上时变宽的过渡动画效果

### CSS3的transition过渡属性值

transition属性是个复合属性, 主要包括以下几个子属性

- transition-property 要进行过渡的属性
- transition-duration 过渡持续的时间
- transition-timing-function 过渡的动画效果
- transition-delay 事件触发到开始过渡的时间

transition属性可以这样写:

	transition-property: width;
	transition-duration: 1s;
	transition-timing-function: linear;
	transition-delay: 0.5s;
	
也可以这样组合起来简写:

	transition: width 1s linear 0.5s;
	
这种简写语法的顺序可以随意, 但值得注意的是, 不管顺序如何, 第一个出现的时间是`transition-duration`, 第二个出现的时间是`transition-delay`
	
#### transition-property

`transition-timing-function`用来指定过渡动画的CSS属性名称

例如

	// 取一个值
	transititon-property: width;
	// 也可以取多个属性值
	transition-property: width height background-color;
	// 也可以取所有值
	transition-property: all;

	
#### transition-duration

`transition-duration`属性主要用来设置一个属性过渡到另一个属性所需的时间，也就是从旧属性过渡到新属性花费的时间长度，俗称持续时间。

例如

	transition-duration: 1s;

#### transition-timing-function

`transition-timing-function`指的是过渡函数, 听见⎡函数⎦不要怕, 只要写上对应动画效果的函数名就可以了

这些动画函数名有`linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`

例如

	transition-timing-function: ease;

详细信息可以看下图:

![](http://img.mukewang.com/5344f1320001481905640812.jpg)

#### transition-delay

transition-delay是指改变元素属性值后多长时间开始执行。

例如

	transition-delay: 0.5s;

---
以上内容部分参考慕课网和《CSS3案例实践》