# wEvent
事件绑定组件

功能：
对某个DOM元素绑定事件，并对这个DOM下的子元素进行事件管理。

示例：
	
	<ul id="viewList">
	    <li>
	        <div class="light">wEvent组件</div>
	        <div>wEvent实现列类似JQuery的live功能</div>
	    </li>
	    <li>
	        <div class="light">wEvent组件</div>
	        <div>wEvent实现列类似JQuery的live功能</div>
	    </li>
	    <li>
	        <div class="light">wEvent组件</div>
	        <div>wEvent实现列类似JQuery的live功能</div>
	    </li>
	</ul>

	wEvent.on({
		rootElement:document.getElementById("viewList"),
		type:"click",
		queryString:"li .light",       //指定rootElement里的 "li .light" 元素的事件响应
		process:function(e){
			alert("你单击了 li元素里class=“light” 的元素");
			alert("被触发的DOM:"+this.targets[".light"]);
			alert("被触发的DOM:"+this.targets["li"]);
	
			//this.cancelEvent = true;  //取消事件处理
		}
	});

