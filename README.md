<html xmlns="http://www.w3.org/1999/xhtml" lang = "zh-CN">
<head>
<meta charset = utf-8 />
<title>js学习练习题</title>
</head>
<body>

	<script>
		计算a,b的值
		var a = (10 * 3 - 4 / 2 + 1) % 2,
			b = 2;
			b %= a + 3;
			document.write(a++);
			document.write('<br>');
			document.write(--b);


		交换a,b的值
		var a = 123,
			b = 234,
			c = a + b;
			a = c - a;
			b = c - a;
		document.write('交换后a = ' + a);
		document.write('<br>');
		document.write('交换后b = ' + b);




		1.计算2的n次幂，n可输入，n为自然数。
		var n = parseInt(window.prompt('2的n次幂'));
		var mul = 1;
		for(var i = 0; i < n; i++){
			mul *= 2;
		}
		console.log(mul);

		2.计算n的阶乘，n可输入
		var n = parseInt(window.prompt('n的阶乘'));
		var mul = 1;
		for(var i = 1; i <= n; i++){
			mul = mul * i;
		}
		console.log(mul);

		3.输入a,b,c三个数字，打印出最大的。
		var a = parseInt(window.prompt('比较三个数的大小，请输入a'));
		var b = parseInt(window.prompt('比较三个数的大小，请输入b'));
		var c = parseInt(window.prompt('比较三个数的大小，请输入c'));
		if(a > b){
			if (a > c) {
				document.write(a);
			}else{
				document.write(c);
			}
		}else {
			if(b > c){
				document.write(b);
			}else{
				document.write(c);
			}
		}

		4.编写一程序，输入一个三位数的正整数，输出时反向输出。如：输入456,输出654。
		var n = parseInt(window.prompt('请输入n'));
		if(n >= 100 && n < 1000){
			var a = n % 10,
				b = ( n - a ) / 10  % 10,
				c = ( n - a - b * 10 ) /100 % 10;
				d = a * 100 + b * 10 + c;
				document.write(d);
		}else{
				document.write("你输入的不是三位正整数")
			}



		alert(typeof(a)); 		//undfined 类型
		alert(typeof(undefined));	//undefined类型
		alert(typeof(NaN));		//nuber类型
		alert(typeof(nall));		//undefined类型
		var a = "123abc";
		alert(typeof( + a));		//number 
		alert(typeof( !! a));		//boolean
		alert(typeof(a + ""));		//String
		alert(typeof(1 == '1'));	//boolean
		alert(typeof(NaN == NaN));	//boolean  flase
		alert(typeof(NaN == undefined));	//boolean  flase
		alert(parseInt("123abc"));		//123  
		var num = 123123.345789;	
		alert(num.toFixed(3));		 //123123.346 toFixed() 取值精度四舍五入
 		
 		alert(typeof(typeof(a)));	//String类型 结果是"undefined"  


 		8.写一个方法：求一个字符串的字节长度。（提示：字符串有一个方法charCodeAt();一个中文占两个字节,一个英文占一个字节。

 		定义和用法
 		charCodeAt()方法可返回指定位置的字符的Uincode编码，这个返回值是0-65535之间的整数。（当返回值<255时，为英文。当返回值>255是，为中文）
 		语法
 		stringObject.charCodeAt(index)

 		eg:
 			var str = 'hello world!'
 			document.write(str.charCodeAt(1)); //输出101
 		）

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
