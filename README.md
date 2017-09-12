# Frontend-Page-Elements-Demo
This folder is created to store ui elements designed by HTML and CSS.

# 1.Navbar_利用伪类实现超级链接的美化
##1.1创建页面html
```
<div class="nav">
		<ul>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
			<li><a href="#">网站栏目</a></li>
		</ul>
	</div>
```
##1.2样式的设置
* 清除li和div本身自带的padding和margin
```
	*{
		padding:0;
		margin:0;
	}
```

* 设置盒子尺寸为960*50，有边框，上下margin为100px,并且盒子居中
设置文字的水平居中
```
	.nav{
			width: 960px;
			height: 50px;
			border: 1px solid red;
			margin: 100px auto;
		}
```

* li去掉圆点，并且左浮动，给宽高撑出高度，120*50px，文字垂直居中（行高=盒子的高）

	```
	.nav ul{
				/*去掉小圆点*/
		list-style: none;
			}
	.nav ul li{
				float: left;
				width: 120px;
				height: 50px;
				text-align: center;
				line-height: 50px;
			}
	```

* a标签必须有宽高（块级存在），小手作用的区域才大
```
.nav ul li a{
			display: block;
			width: 120px;
			height: 50px;
		}
```
* a没有点击，访问后的样式一致，逗号可以将两个选择器合并
```
		.nav ul li a:link , .nav ul li a:visited{
			text-decoration: none;
			background-color: purple;
			color:white;
		}
```
*鼠标悬停的背景色和字体颜色变化
```
.nav ul li a:hover{
		background-color: yellow;
		color: black;
	}
```

