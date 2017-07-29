### clamp非webkit内核浏览器实现
***

解决方法一,只适合于英文文本,英文单次都使用空格间隔单词。

js

	var ellipsisText = function (e, etc) {
    	var wordArray = e.innerHTML.split(" ");
    	while (e.scrollHeight > e.offsetHeight) {
       	 	wordArray.pop();
       	 	e.innerHTML = wordArray.join(" ") + (etc || "...");
    	}
	};
	
html

	<div class="block-with-text">
    	Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod  tempor incidi ut aliquip ex ea commodo consequat sum dolor sit 123
	</div>
	
css 

	.block-with-text {
    	line-height: 1.4em;
   	 	max-height: 5.6em; /* max: 4 lines */
	}
	
js

	[].forEach.call(document.querySelectorAll(".block-with-text"), function(elem) {
    ellipsisText(elem);
	});
	
	
解决方法二,遍历所有文本,性能较差。


	<div class="figcaption"><p>作为微软的游戏平台，Xbox已经出现在了Windows Phone和Windows 8中，就在最近，微软宣布将旗下的Zune消费品牌也一并整合至Xbox品牌下，Xbox Live服务影响力越来越大，渗透面也越来越广。</p></div>
	
	
	
js

	$(".figcaption").each(function(i){
    	var divH = $(this).height();
    	var $p = $("p", $(this)).eq(0);
    	while ($p.outerHeight() > divH) {
       		 $p.text($p.text().replace(/(\s)*([a-zA-Z0-9]+|\W)(\.\.\.)?$/, "..."));
    	};
	});
	
解决方法三,js和css结合。

step1.给需要截断的段落，新增css

	.sfc-poi-dtl-comment-ff{
		position: relative;
    	line-height: 23px;
    	height: 68px;
   	 	overflow: hidden;
	}
	.sfc-poi-dtl-comment-ff:after{
   		content: "...";
   	 	font-weight: bold;
   	 	position: absolute;
   		bottom: 0;
   		right: 0;
  		padding: 0 5px 0 10px;
   	 	background: -moz-linear-gradient( 0% 90% 		360deg,rgba(255, 255, 255, .5),rgba(255, 255, 255, 1));
	}	
	
step2.计算元素的高度范围，符合要求新增class

	/*firefox*/
    var na = navigator.userAgent.toLowerCase();
    if(na.indexOf("firefox") > 0) {  
        var $commentEle = $container.find('.sfc-poi-dtl-comment-text');
        var flag = true;
        while ($commentEle.height() > 68 && flag){
        	$commentEle.addClass('sfc-poi-dtl-comment-ff');
            flag = false;
        }
        $container.find('.sfc-poi-dtl-comment-text').on('click', showText);
        function showText(e) {
            var target = $(e.target);
            if (target.hasClass('sfc-poi-dtl-comment-ff')) {
                target.removeClass('sfc-poi-dtl-comment-ff');
            } else {
                target.addClass('sfc-poi-dtl-comment-ff');
            }
        }
    }