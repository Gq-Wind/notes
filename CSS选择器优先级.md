### CSS选择器优先级

```
通配符 0
标签 伪元素 0 0 0 1
类 状态伪类 结构伪类 属性 0 0 1 0
id  0 1 0 0
内联样式style 1 0 0 0
!important 无穷大
```

#### 复合选择器

​	关系选择器

- 后代
- 子类 >
- 兄弟 + (邻接)   ~(通用)
- 交集
- 并集 ,

> 复合权重为基础权重累加

> ‼️ 伪类：a:hover、p:first-child 的权重是0,0,1,1 不是 0,0,1,0；a:nth-of-type(n):hover权重是 0,0,2,1;**即要加上前面那个元素的权重**。

属性选择器:

```
= 完全相等
~ (可能有多一个属性,匹配一个)
子字符串匹配:^ $ *(出现)
i大小写敏感:	
li[class^="a" i]
```



---

状态伪类:`link visited hover active focus`

结构伪类:

```
:first-child 选择某个元素的第一个子元素；  
:last-child 选择某个元素的最后一个子元素；
:nth-child(n) 匹配属于其父元素的第 n个子元素，不论元素的类型；
:nth-last-child() 从这个元素的最后一个子元素开始算,选匹配属于其父元素的第 n个子元素，不论元素的类型；
:nth-of-type() 规定属于其父元素的第n个 指定 元素；
:nth-last-of-type() 从元素的最后一个开始计算,规定属于其父元素的指定 元素；
:first-of-type 选择一个上级元素下的第一个同类子元素；
:last-of-type 选择一个上级元素的最后一个同类子元素；
:only-child 选择它的父元素的唯一一个子元素；
:only-of-type 选择一个元素是它的上级元素的唯一一个相同类型的子元素；
:checked匹配被选中的input元素，这个input元素包括radio和checkbox。
:empty 选择的元素里面没有任何内容。
:disabled匹配禁用的表单元素。
:enabled匹配没有设置disabled属性的表单元素。
:valid匹配条件验证正确的表单元素。
:in-range选择具有指定范围内的值的 <input> 元素。
:optional选择不带 "required" 属性的 <input> 元素。
:focus选择获得焦点的 <input> 元素。
```

伪元素:`after before first-line`

创建一些不在文档树中的元素，并为其添加样式

---

#### 继承性

1. 字体系列属性
2. 文本系列属性
   1. 内联元素 color line-height word-spacing letter-spacing 
   2. 块级元素 text-indent text-align
3. 元素可见性:visibility

⚠️不可继承

1. display
2. 盒子模型属性 width height margin border padding
3. 背景属性 
4. 定位属性

---

Background-clip:控制元素背景是否延伸到盒子边框 内边距盒子 内容盒子下面 border-box content-box padding-box text(背景被裁成文字的前景色)

`background: linear-gradient url position repeat attachment`

> attachment: scroll(相对于元素本身) fixed(相对于视窗) local(相对于元素的内容)

---

### 外部显示类型

块级盒子和父级一样宽;每个盒子都会换行;width height 可以发挥作用;padding margin  border可以将其他元素推开

> 内部显示类型:决定了盒子内部是如何布局的;在一个元素上，外部显示类型是 `block`，但是内部显示类型修改为 `flex`,该盒子的所有直接子元素都会成为 flex 元素，会根据[弹性盒子（Flexbox）](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout/Flexbox)规则进行布局

内联盒子不换行;width height 不起作用;垂直方向的margin padding border被应用,但是不把其他linline盒子推开;



