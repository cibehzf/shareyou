<link rel="stylesheet" href="http://yandex.st/highlightjs/6.1/styles/default.min.css">
<script src="http://yandex.st/highlightjs/6.1/highlight.min.js"></script>
<script>
    hljs.tabReplace = '    ';
    hljs.initHighlightingOnLoad();
</script>

### CSS3动画使用入门

1. 定义动画名和动画**关键帧**

		@keyframe changecolor{
			0%{
				background-color: red;
			}
			50%{
				background-color: orange;
			}
			100%{
				background-color: yellow;
			}
		}
		
	说明: changecolor是自定义的动画名,0%, 50%, 100%是定义关键帧

2. 定义元素的原始状态

		.demo{
			backgroundcolor: red;
		}
	
3. 使用keyframes定义好的动画

		.demo{
			background: red;
			animation: changecolor 5s ease 0.2s;
		}

通过以上三步, 就能实现简单的背景颜色变化的动画效果.

### @keyframes介绍

案例:

	@keyframe changecolor{
		0%{
			background-color: red;
		}
		50%{
			background-color: orange;
		}
		100%{
			background-color: yellow;
		}
	}
	
- changecolor是动画名, 可以自定义自己想要的动画名称
- 0%, 50%, 100%是定义的关键帧
	- 关键帧指的是第一帧要执行什么变化, 第二帧要执行什么变化, 第n帧要执行什么变化
	- 0%, 50%, 100%指的是不懂的帧数, 可以在0%~100%之内自定义想要的帧数

### animation动画属性值

transition属性是个复合属性, 主要包括以下几个子属性

- animation-name
- animation-duration
- animation-timing-function
- animation-delay
- animation-iteration-count
- animation-direction
- animation-play-state
- animation-fill-mode

animation可以这样写:

	animation-name: changecolor;
	animation-duration: 5s;
	animation-timing-function: ease;
	animation-delay: 0.2s;
	
也可以这样写:

	animation: changecolor 5s ease 0.2s;
	// 这些属性值可以打乱, 但最前面的时间值一定是animation-duration
	
#### animation-name

用来定义动画的名称

例如

	animation-name: changecolor;
	// 或者
	animation-name: wholle;

名称可以自由定义

注意: animation-name 调用的动画名需要和“@keyframes”定义的动画名称完全一致（区分大小写）

#### animation-duartion

设置动画播放时间, 完成@keyframes从0%~100%一次动画所需的时间

例如;

	animation-duration: 5s;
	
#### animation-timing-function

定义动画函数, 写上动画函数

听见⎡函数⎦不要怕, 只要写上对应动画效果的函数名就可以了

这些动画函数名有`linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`

对应的动画方式

![](http://img.mukewang.com/534b8bb100016e9f05690795.jpg)

例如

	animation-timing-function: ease;
	
#### animation-delay

定义开始执行动画之前等待的时间;

例如

animation-delay: 0.5s;

#### animation-iteration-count

定义动画播放的次数

例如

ainimation-iteration-count: 5;

上例取值是5, 意思是播放五次. 如果取值为infinite, 动画将无限次播放.

#### animation-direction

定义动画方向

参数有

- normal 默认值, 每次循环都是向前播放
- alternate, 第一次向前播放, 第二次反方向播放

例如

	animation-direction: alternate;
	
#### animation-play-state

设置动画的播放状态

参数有

- running 默认值 动画播放
- paused 动画暂停

#### animamtion-fill-mode

定义开始之前和结束之后发生的操作

参数有

- none 默认值 表示动画将按预期进行和结束，在动画完成其最后一帧时，动画会反转到初始帧处
- forwards 表示动画在结束后继续应用最后的关键帧的位置
- backwards 会在向元素应用动画样式时迅速应用动画的初始帧
- both 元素动画同时具有forwards和backwards效果

例如

	animation-fill-mode:forwards; 