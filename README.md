# wEvent
事件绑定组件

功能：
对某个DOM元素绑定事件，并对这个DOM下的子元素进行事件管理。

示例：
	<ul id="viewList" class="viewList">
		<li dataid="001">
			<div class="light">20123年2月2日</div>
			<div>
				<span>数据信息</span>
			</div>
		</li>
		<li dataid="002">
			<div class="light">20123年3月12日</div>
			<div>
				<span>信息数据</span>
			</div>
		</li>
		<li dataid="003">
			<div class="light">20123年3月21日</div>
			<div>
				<span>wEvent组件</span>
			</div>
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

