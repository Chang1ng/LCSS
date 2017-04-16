### background-origin/size/clip
***

origin
取值：

* border-box   从边框开始放置背景图片
* padding-box   从padding值开始放置背景图片
* content-box    从内容块开始放置图片，不包括padding和border

size
取值：

* 百分比   一般常用的为100% 100% （宽高都为100%）
* 具体数值    比如100px 100px （如果只填写一个值，那么默认是宽度，高度是auto，auto为等比缩放后的值）
* auto  默认值，背景图像的真实大小
* cover 等比例放大到容器可以盛放的大小，可能超出容器的范围
* contain 等比缩放比例和容器的宽高比例一致，通常图片会不足以填充满容器。

clip
取值：
* border-box 默认值，无实际效果
* padding-box 边框不受影响
* content-box 仅仅只是内容区域有背景图片
* text 文字以外的其他部分没有任何背景图片，适合做文字CSS3特效

