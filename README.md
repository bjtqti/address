#省市区三级联动地址下拉选择框

===

##怎么使用？

参考index.html

文件说明： 
	"region.js" 地区数据库文件
	"selector.js" 程序文件
    "selector.css" 样式文件
页面设置：
    仅需要定一个id就好了
```html
	<div id="address"></div>
```
程序调用：
```javascipt
	var wrap = document.getElementById('address');
	var a = new Selector(wrap,{
		data:data
	});
	//如果有默认选择的地址
	var a = new Selector(wrap,{
		data:data,
		pid:'430000',	//湖南
		cid:'430300',
		aid :'430381'
	});
	//获取地址信息
	var rs = a.getAddress();
	// rs同时包含了地址名和地址的id
```