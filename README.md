<html xmlns="http://www.w3.org/1999/xhtml" lang = "zh-CN">
<head>
<meta charset = utf-8 />
<title>js学习</title>
</head>
<body>

	<script>

		
 		// 8.写一个方法：求一个字符串的字节长度。（提示：字符串有一个方法charCodeAt();一个中文占两个字节,一个英文占一个字节。

 		// 定义和用法
 		// charCodeAt()方法可返回指定位置的字符的Uincode编码，这个返回值是0-65535之间的整数。（当返回值<255时，为英文。当返回值>255是，为中文）
 		// 语法
 		// stringObject.charCodeAt(index)

 		// eg:
 		// 	var str = 'hello world!'
 		// 	document.write(str.charCodeAt(1)); //输出101
 		// ）

 		var str = window.prompt("请输出字符串");
 		function bytelength(str){
 			var that = str.length;
 			for(var i = 0; i < str.length; i++){
 				if(str.charCodeAt(i)>255){
 					that++;
 				}
 			} 
 			return that;
 		}
 		console.log(bytelength(str));


	</script>
	
</body>
</html>
