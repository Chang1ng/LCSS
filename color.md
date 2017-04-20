### color
***

> **rgba**
> rgb--三原色光模式

实现元素背景透明不影响子元素可以这样：
	`background-color:rgba(0,0,0,.5)`
参数分别为：red红色值，green值，blue值，alpha透明值。值可以是数值或者百分比。

不约束取值范围，渲染成最接近的颜色：
	`background-color:rgba(-1,-1,-1,1)` 等价于
	`background-color:rgba(0,0,0,1)`

transparent等价于`rgba(*,*,*,0)`

> **colorName**
> 英文单词来代表颜色关键字

black
silver
gray
white
maroon
red
purple
fuchsia
green
lime
olive
yellow
navy
blue
teal
aqua


> **HEX**
> 十六进制记法,取值形如：#RRGGBB 或 #RGB

取值范围为：00 - FF。
参数必须是两位数。对于只有一位的，应在前面补零。
如果每个参数各自在两位上的数字都相同，那么本单位也可缩写为 #RGB 的方式。例如：#33FF00 可以缩写为 #3F0。
此色彩模式与RGB色彩模式不同。

> **HSL/HSLA**
> 取值形如：HSL(H,S,L)

H：Hue(色调)。0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。取值为：0 - 360
S：Saturation(饱和度)。取值为：0.0% - 100.0%
L：Lightness(亮度)。取值为：0.0% - 100.0%

> **currentColor**
> 取值继承color的值，如果直接应用在color本身，取值inherit

    div{
	    border:1px solid;//取值为green
	    color: green;
    }