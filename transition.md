### transition

transition用于实现css简单的过渡动画，类似于flash的补间动画。
***

### 属性

1. transition-propert  			过渡的css属性.通常取值为all，none，某些css属性
2. transition-duration 			过渡时间
3. transition-timing-function  过渡效果，默认是ease.通常取值为：linear匀速，ease慢快慢，ease-in先慢后快，ease-out先快后慢，ease-in-out慢速开始快速结束，cubic-bezier(n,n,n,n)自定义运动轨迹
4. transition-delay 			过渡延迟时间。默认是0，值可以为s或者ms
5. transition					所有属性的集合简写形式


### 举例

默认样式

	div{
		width:100px;
		height:100px;
		transition-property:width,height;
		transition-duration:1s;
		transition-timing-function:linear;
		transition-delay:2s;
		
		/*safari*/
		-webkit-transition-property:width,height;
		...
	}
	
	div:hover{
		width:200px;
		height:200px;
	}
