# 对话框组件效果说明 #
=============================
+ 1、 组件介绍
	原生JS实现，不需要依赖任何js库。实现了兼容pc与手机端，所有的参数都可以修改。
+ 2、 使用方法
	| 在HTML中擦创建一个id名为swipe的div; |  
	| hukW:字符串，宽度; |  
	| guan:数字，为1时禁用右上角的x号按钮，默认为0; |  
	| bacolor:可以设置对话框的背景颜色,也可以不设置，默认为白色; |  
	| que:按钮的id; |  
	| quxiao:取消按钮；|  
	| tit:标题; |  
	| tit1:内容; |  
	| tit2:详细内容; |  
	例如：
		HTML代码：
			<button id="xin">显示对话框1</button>
			<div class="kaung">
				<div class="hu_title">
					<p></p>
					<button class="guan" id="hu_guan">×</button>
				</div>
				
				<div class="hu_nr">
					<h4>2</h4>
					<p></p>
				</div>
				
				<div class="hu_an">
					<button id="hu_que" class="hu_ann">确认</button>
					<button id="hu_qu" class="hu_ann">取消</button>
				</div>
				
			</div>
			<div class="hu_in"></div>
		js链接：
			<script src="dist/alert_gh-1.1.0.min.js"></script>
		css链接：
			写在网页的最上面
			<link rel="stylesheet" href="dist/alert.css">
		JS代码：
			var xin = document.querySelector("#xin");
			var xinxx = document.querySelector("#xinxx");
			xin.onclick = function(){
			// 初始化参数
			var obj = {
				hukW:"500",// 绘画框的宽度,如果不设置默认值为300px;
				guan:0, //为1时禁用右上角的x号按钮，默认为0;
				bacolor:"#fff", // 可以设置对话框的背景颜色,也可以不设置，默认为白色
				guanl:function(){
					// 用户点击右上角x号时调用的函数，该参数可有可无
					console.log("X");
				},
				que:que,
				quxiao:quxiao,
				tit:"标题",
				tit1:"内容",
				tits:"内容详细"
			}
			var dui = new Huihua(obj);
			dui.xian(); // 调用xian()方法显示对话框
			function que(){
				//确认回调的函数
				console.log("确认")
			}
			function quxiao(){
				//取消回调的函数
				return false;
			}
+ 3、 回调函数
	用户在点击完成之后继续操作必须写到此回调函数中
	例如：
	//点击确定的回调函数
	function que(transPercent){
		console.log("确认");
	}
	//点击取消的回调函数
	function quxiao(transPercent){
		console.log("取消");
	}
+ 4、 联系方法
	邮箱：2221273125@qq.com