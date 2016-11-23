# -
Jquery学习
1.jquery选择器
	jquery元素选择器和属性选择器允许你通过标签名、属性名或内容对HTML元素进行选择
	(1)jQuery 元素选择器
		$("p")选取所有的p元素
		$("p.intro") 选取所有 class="intro" 的 <p> 元素。
		$("p#demo") 选取所有 id="demo" 的 <p> 元素。
	(2)jQuery 属性选择器
		jQuery 使用 XPath 表达式来选择带有给定属性的元素。
		$("[href]") 选取所有带有 href 属性的元素。
		$("[href='#']") 选取所有带有 href 值等于 "#" 的元素。
		$("[href!='#']") 选取所有带有 href 值不等于 "#" 的元素。
		$("[href$='.jpg']") 选取所有 href 值以 ".jpg" 结尾的元素。
	(3)jQuery CSS 选择器
		jQuery CSS 选择器可用于改变 HTML 元素的 CSS 属性。
		$("p").css("background-color","red");
	(4)更多选择器实例
		$(this)当前的HTML元素
		$("ul li:first")每个ul的第一个li元素
		$("[href$='.jpg']")所有带有以 ".jpg" 结尾的属性值的 href 属性
		$("div#intro .head") id="intro" 的 <div> 元素中的所有 class="head" 的元素
2.Jquery事件
	（1）jQuery 事件处理方法是 jQuery 中的核心函数。
	（2）jQuery 名称冲突
		 jQuery 使用 $ 符号作为 jQuery 的简介方式。
		 某些其他 JavaScript 库中的函数（比如 Prototype）同样使用 $ 符号。
		 jQuery 使用名为 noConflict() 的方法来解决该问题。
		 var jq=jQuery.noConflict()，帮助您使用自己的名称（比如 jq）来代替 $ 符号。
	（3）jquery的一些事件
		$(document).ready(function)  	将函数绑定到文档的就绪事件（当文档完成加载时）
		$(selector).click(function)     触发或将函数绑定到被选元素的点击事件
		$(selector).dblclick(function)  触发或将函数绑定到被选元素的双击事件
		$(selector).focus(function)     触发或将函数绑定到被选元素的获得焦点事件
		$(selector).mouseover(function) 触发或将函数绑定到被选元素的鼠标悬停事件
3.jquery隐藏/显示
	 $("p").show()函数;
	 $("p").hide()函数;
	 $(selector).hide(speed,callback);//speed 参数规定隐藏/显示的速度可以取"slow"、"fast" 或毫秒。
	 $(selector).show(speed,callback);//可选的 callback 参数是隐藏或显示完成后所执行的函数名称。
	 jQuery toggle()函数//使用toggle()方法来切换hide()和show()方法
4.jquery淡入淡出
	jQuery fadeIn()  jQuery fadeIn()用于淡入已隐藏的元素。
	jQuery fadeOut() 方法用于淡出可见元素。
	jQuery fadeToggle() 方法可以在 fadeIn() 与 fadeOut() 方法之间进行切换。
	jQuery fadeTo() 方法允许渐变为给定的不透明度（值介于 0 与 1 之间）。
5.jquery滑动效果
	jQuery slideDown() 方法用于向下滑动元素。
	jQuery slideUp() 方法用于向上滑动元素。
	jQuery slideToggle() 方法可以在 slideDown() 与 slideUp() 方法之间进行切换。
6.jquery动画
	jQuery animate() 方法用于创建自定义动画。
	$(selector).animate({params},speed,callback);
	必需的 params 参数定义形成动画的 CSS 属性。
	可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。
	可选的 callback 参数是动画完成后所执行的函数名称。
	
	
	jQuery stop() 方法用于停止动画或效果，在它们完成之前。
	
7.jQuery Chaining
	$("#p1").css("color","red").slideUp(2000).slideDown(2000);
8.jquery获取内容的方法
	text() - 设置或返回所选元素的文本内容
	html() - 设置或返回所选元素的内容（包括 HTML 标记）
	val()  - 设置或返回表单字段的值
9.jQuery attr() 方法用于获取属性值。
10.jquery添加
	append() - 在被选元素的结尾插入内容   （里面）
	prepend() - 在被选元素的开头插入内容（里面）
	after() - 在被选元素之后插入内容（外面）
	before() - 在被选元素之前插入内容（外面）
11.jquery删除
	jQuery remove() 方法删除被选元素及其子元素。
	jQuery empty() 方法删除被选元素的子元素。
	过滤被删除的元素
	$("p").remove(".italic");  删除 class="italic" 的所有 <p> 元素
12.jQuery CSS 类
	addClass() - 向被选元素添加一个或多个类
	removeClass() - 从被选元素删除一个或多个类
	toggleClass() - 对被选元素进行添加/删除类的切换操作
	css() - 设置或返回样式属性
13.jquery尺寸
	width()     设置或返回元素的宽度（不包括内边距、边框或外边距）
	height()	设置或返回元素的高度（不包括内边距、边框或外边距）
	innerWidth()返回元素的宽度（包括内边距）。
	innerHeight()返回元素的高度（包括内边距）
	outerWidth()返回元素的宽度（包括内边距和边框）
	outerHeight()返回元素的高度（包括内边距和边框）。
	$("button").click(function(){
	  $("#div1").width(500).height(500);
	});//设置div宽度和高度
14.Jquery遍历-祖先
	parent()	parent() 方法返回被选元素的直接父元素。
	parents()	parents() 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素 (<html>)
	parentsUntil()	parentsUntil() 方法返回介于两个给定元素之间的所有祖先元素。
15.Jquery遍历-后代
	children() 方法返回被选元素的所有直接子元素。
	find() 方法返回被选元素的后代元素，一路向下直到最后一个后代。
16.Jquery遍历-同胞
	siblings()	siblings() 方法返回被选元素的所有同胞元素。
	next()		next() 方法返回被选元素的下一个同胞元素。
	nextAll()	nextAll() 方法返回被选元素的所有跟随的同胞元素。
	nextUntil()	nextUntil() 方法返回介于两个给定参数之间的所有跟随的同胞元素。
	prev()	prev(), prevAll() 以及 prevUntil() 方法的工作方式与上面的方法类似，只不过方向相反而已：它们返回的是前面的同胞元素（在 DOM 树中沿着同胞元素向后遍历，而不是向前）。
	prevAll()
	prevUntil()
17.Jquery遍历-过滤
	jQuery first() 方法  first() 方法返回被选元素的首个元素。
	
	jQuery last() 方法 	last() 方法返回被选元素的最后一个元素。
	
	jQuery eq() 方法	eq() 方法返回被选元素中带有指定索引号的元素。
	
	filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。
	
	not() 方法返回不匹配标准的所有元素。not() 方法与 filter() 相反。
	
