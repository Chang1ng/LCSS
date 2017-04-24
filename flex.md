### Flex

#### Flex历史版本
	display: -webkit-box;
	
	display: -ms-flexbox;
	
	display: -webkit-flex;
	
	display: flex;

#### Flex按照指定方向排列元素
	flex-direction:row;
	flex-direction:row-reverse;
	flex-direction:column;
	flex-direction:column-reverse;

#### Flex随意指定排序
order:1(指定顺序值)

	/* Numerical value including negative numbers */
	order: 5;
	order: -5;

	/* Global values */
	order: inherit;
	order: initial;
	order: unset

[order](https://developer.mozilla.org/zh-CN/docs/Web/CSS/order "火狐开发者中心")


#### Flex横轴分布空间
	justify-content: flex-start;
	justify-content: flex-end;
	justify-content: center;
	justify-content: space-between;
	justify-content: space-around;

[justify-content](https://developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content "火狐开发者中心")

#### align-items 纵轴分布空间
flex-start：弹性盒子元素的侧轴起始位置的边界紧靠住该行的侧轴起始边界

flex-end：弹性盒子元素的侧轴起始位置的边界紧靠住该行的侧轴结束边界

center：弹性盒子元素在该行的侧轴上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）

baseline：如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐

stretch：如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制

#### flex-wrap子元素换行
nowrap - 默认， 弹性容器为单行。该情况下弹性子项可能会溢出容器

wrap - 弹性容器为多行。该情况下弹性子项溢出的部分会被放置到新行，子项内部会发生断行

wrap-reverse -反转 wrap 排列

#### align-content
align-content 属性用于修改 flex-wrap 属性的行为。类似于 align-items, 但它不是设置弹性子元素的对齐，而是设置各个行的对齐

	flex-start 
	flex-end 
	center
	space-between
	space-around
	stretch

#### align-self 子元素自身的纵轴对齐

	auto 
	flex-start 
	flex-end
	center 
	baseline 
	stretch

#### flex-flow = flex-direction flex-wrap

	
