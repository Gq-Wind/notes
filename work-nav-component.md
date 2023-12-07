### 响应式导航栏参照

```
//纯html css控制, @media查询实现响应式,css控制样式显示隐藏
<nav id="top">
			
			<div class="logo">
				<img src="pic/logo2.png" />
			</div>
			
			<div class="nav-text">
				
				<input type="checkbox" id="check" />
				<label for="check" class="checkbtn">
					<i class="fa fa-bars"></i>
				</label>
				
				
				<ul class="nav-titles">
					<li class="nav-title">
						Home
					</li>
					<li class="nav-title">
						<div class="nav-link">Project</div>
						<div class="nav-substitle">
							<a>Design</a>
							<a>Description</a>
							<a>Contribution</a>
							<a>Safety</a>
						</div>
					</li>
					<li class="nav-title">
						<div class="nav-link">Project</div>
						<div class="nav-substitle">
							<a>Design</a>
							<a>Description</a>
							<a>Contribution</a>
							<a>Safety</a>
						</div>
					</li>
					<li class="nav-title">
						<div class="nav-link">Project</div>
						<div class="nav-substitle">
							<a>Design</a>
							<a>Description</a>
							<a>Contribution</a>
							<a>Safety</a>
						</div>
					</li>
				</ul>
				
			</div>
			
		</nav>
	</body>
	
	*{
	padding: 0;
	margin: 0;
}
#top{
	background-color: #000000;
	height: 70px;
	position: fixed;
	width: 100%;
}
.logo img{
	width: 100%;
	border-radius: 100px;
}
.logo{
	background-color: #000000;
	position: absolute;
	width: 7%;
	border-radius: 80px;
}
.nav-text{
	width: fit-content;
	margin: auto;
}
.nav-title{
	display: inline-block;
	height: 60px;
	text-align: center;
	line-height: 70px;
	width: 100px;
	color: white;
	vertical-align: top;
}
.nav-substitle{
	background-color: #353535;
	border-radius: 5px;
	line-height: 50px;
	width: 200px;
	display: none;
	opacity: 0.8;
}
.nav-substitle a{
	display: block;
	border: 3px solid transparent;
}
.nav-substitle a:hover{
	border: 3px solid white;
	transition-duration: 0.3s;
	border-radius: 5px;
	opacity: 1;
}
.nav-title:hover{
	cursor: pointer;
	border-bottom: 3px solid white;
	transition-duration: 1s;
}
.nav-link:hover ~ .nav-substitle{
	display: block;
}
.nav-substitle:hover{
	display: block;
}
.checkbtn{
	font-size: 30px;
	color: white;
	float: right;
	line-height: 70px;
	margin-right: 40px;
	cursor: pointer;
	display: none;
}
#check{
	display: none;
}
@media (max-width: 858px) {
	.checkbtn{
		display: block;
	}
	.logo{
		width: 60px;
	}
	ul{
		position: fixed;
		width: 100%;
		height: 100%;
		background: #2c3e50;
		top: 70px;
		left: -100%;
		text-align: center;
		transition: all 0.5s;
	}
	nav ul li{
		display: block;
		margin: 20px 0;
		line-height: 20px;
	}
	.nav-title{
		width: 100%;
	}
	nav ul li a{
		font-size: 20px;
	}
	.nav-substitle{
		width: 100%;
		position: relative;
		top: -5px;
	}
	#check:checked ~ ul{
		left: 0;
	}
	.nav-text{
		width: 100%;
	}
}
这里比较特殊的是hamberger部分,check:checked

```

纯css主要通过@media和hover实现

#### vue组件实现导航栏

v-show



































> Less: 
>
> ```less
> @var_name: attribute; //变量
> 
> .bordered {
> 	border-top:dotted 1px black;
>   border-bottom: solid 2px black;
> }
> .post a {
>   color: red;
>   .bordered(); //混入
> }
> //转义
> @min768: ~"(min-width: 768px)";
> .element {
>   @media @min768 {
>     font-size: 1.2rem;
>   }
> }
> #bundle() { 	// 命名空间 #bundle
>   .button {
>     display: block;
>     border: 1px solid black;
>     background-color: grey;
>     &:hover {
>       background-color: white;
>     }
>   }
>   .tab { ... }
>   .citation { ... }
> }
> //命名空间 映射
> #colors() {
>   primary: blue;
>   secondary: green;
> }
> 
> .button {
>   color: #colors[primary];
>   border: 1px solid #colors[secondary];
> }
> ```
>
> 

