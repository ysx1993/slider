slider.js使用说明
slider.js是基于jquery所开发出来的一个画面切换插件

初始化：
<div class="slider-box">
	<ul>
		<li></li>
	</ul>
</div>

把ul和li添加到你的div中,ul元素只能是一个,li元素若干,li元素会充满这个div.

调用方法:
var slider = $(".slider-box").slider({
	 direction:"vertical", //上下切换, 默认"horizontal"
     index: 2,  //初始化所在页面, 默认0
     autoplay:true, //是否自动切换, 默认false
     speed:600, //切换速度, 默认500
     interval:1000, //切换间隔, 默认1000
     easing: "easeInQuart", //切换效果, 默认"linear"
     end:function(){ //每次切换完毕调用, 默认空
     },
     start:function(){ //每次切换开始调用, 默认空
         $("#show").text("current page: " + slider.index);
     },
     prevBtn:"#btn1", //把向左切换的功能绑定到"#btn1"中,此参数还可支持dom元素,jquery元素, 默认空
     nextBtn:"#btn2", //同上
     touch: true, //手机上支持触摸切换, 默认false
     key:true //支持键盘切换, 默认false
})

关键属性:
index 指示当前页面序号 

关键方法:
prev() 切换到上一画面
next() 切换到下一画面
to() : 切换到指定画面
autoPlay() : 自动切换
stopPlay() : 停止自动切换

支持的缓动:
linear，swing，jswing，easeInQuad，easeOutQuad，easeInOutQuad，easeInCubic， easeOutCubic，easeInOutCubic，easeInQuart，easeOutQuart，easeInOutQuart， easeInQuint，easeOutQuint，easeInOutQuint，easeInSine，easeOutSine， easeInOutSine，easeInExpo，easeOutExpo，easeInOutExpo，easeInCirc， easeOutCirc，easeInOutCirc，easeInElastic，easeOutElastic，easeInOutElastic， easeInBack，easeOutBack，easeInOutBack，easeInBounce，easeOutBounce，easeInOutBounce
