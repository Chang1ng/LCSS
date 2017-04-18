### transform
***
2D transform

> matrix(n,n,n,n,n,n)	定义 2D 转换，使用六个值的矩阵。
> translate(x,y)	        定义 2D 转换，沿着 X 和 Y 轴移动元素。
> translateX(n)	        定义 2D 转换，沿着 X 轴移动元素。
> translateY(n)	定义 2D 转换，沿着 Y 轴移动元素。
> scale(x,y)	定义 2D 缩放转换，改变元素的宽度和高度。
> scaleX(n)	定义 2D 缩放转换，改变元素的宽度。
> scaleY(n)	定义 2D 缩放转换，改变元素的高度。
> rotate(angle)	定义 2D 旋转，在参数中规定角度。
> skew(x-angle,y-angle)	定义 2D 倾斜转换，沿着 X 和 Y 轴。
> skewX(angle)	定义 2D 倾斜转换，沿着 X 轴。
> skewY(angle)	定义 2D 倾斜转换，沿着 Y 轴。

3D transform属性

> transform	向元素应用 2D 或 3D 转换。	
> transform-origin	允许你改变被转换元素的位置。	
> transform-style	规定被嵌套元素如何在 3D 空间中显示。	 flat(子元素不保留3D空间)  preserve-3d(子元素保留3D空间)
> 当为元素定义 perspective 属性时，其子元素会获得透视效果，而不是元素本身。
> perspective	规定 3D 元素的透视效果。	
> perspective-origin	规定 3D 元素的底部位置。	
> backface-visibility	定义元素在不面对屏幕时是否可见。visible背景可见，hidden背景不可见	

3D transform function

> matrix3d(n,n,n,n,n,n,n,n,n,n,n,n,n,n,n,n)	定义 3D 转换，使用 16 个值的 4x4 矩阵。
> translate3d(x,y,z)	定义 3D 转化。
> translateZ(z)	定义 3D 转化，仅使用用于 Z 轴的值。
> scale3d(x,y,z)	定义 3D 缩放转换。
> scaleZ(z)	定义 3D 缩放转换，通过给定一个 Z 轴的值。
> rotate3d(x,y,z,angle)	定义 3D 旋转。
> rotateX(angle)	定义沿 X 轴的 3D 旋转。
> rotateY(angle)	定义沿 Y 轴的 3D 旋转。
> rotateZ(angle)	定义沿 Z 轴的 3D 旋转。
> perspective(n)	定义 3D 转换元素的透视视图。