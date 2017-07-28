### clamp
***

1.解决方法

js

	var ellipsisText = function (e, etc) {
    	var wordArray = e.innerHTML.split(" ");
    	while (e.scrollHeight > e.offsetHeight) {
       	 	wordArray.pop();
       	 	e.innerHTML = wordArray.join(" ") + (etc || 			"...");
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
	
	
2.解决方法


	<div class="figcaption"><p>作为微软的游戏平台，Xbox已经出现在了Windows Phone和Windows 8中，就在最近，微软宣布将旗下的Zune消费品牌也一并整合至Xbox品牌下，Xbox Live服务影响力越来越大，渗透面也越来越广。</p></div>
	
	
	
js

	$(".figcaption").each(function(i){
    	var divH = $(this).height();
    	var $p = $("p", $(this)).eq(0);
    	while ($p.outerHeight() > divH) {
       		 $p.text($p.text().replace(/(\s)*([a-zA-Z0-9]+|\W)(\.\.\.)?$/, "..."));
    	};
	});