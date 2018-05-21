#### meta 标签
- name='viewport'//实现一些移动端适配的参数

#### flex弹性布局

    flex: 1
    
让所有弹性盒模型对象的子元素都有相同的长度，且忽略他们内部的内容。

##### flex容器
任何容器都可以flex布局。Flex容器的所有子元素也自动成为容器的成员，成为Flex项目。Flex容器默认存在2根轴线（水平主轴和垂直交叉轴）,布局就是根据这2根轴来排列项目显示的。

	块级元素：display:flex;
	内联元素：display:inlne-flex;

 使用了flex布局后，项目的**float、clear、vertical-align**都将失去效果。

##### Flex容器属性
- flex-direction：设置项目的排列方向

    flex-direction: row | row-reverse | column | column-reverse;

- flex-wrap：设置项目是否换行排列

    flex-wrap: nowrap | wrap | wrap-reverse; 
 
 - flex-flow：flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap
 
     flex-flow: <flex-direction> || <flex-wrap>;
 
 - justify-content：设置项目的水平对齐方式
 
     justify-content: flex-start | flex-end | center | space-between | space-around;
 
  flex-start（默认值）：左对齐
  flex-end：右对齐
  center： 居中
  space-between：两端对齐，项目之间的间隔都相等。
  space-around：每个项目两侧的间隔相等。所以，项目   之间的间隔比项目与边框的间隔大一倍。

- align-items：设置项目垂直方向对齐方式。
   
     align-items: flex-start | flex-end | center | baseline | stretch;
flex-start：交叉轴的起点对齐。
flex-end：交叉轴的终点对齐。
center：交叉轴的中点对齐。
baseline: 项目的第一行文字的基线对齐。
stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。

##### 
#### css hack
- 简述

  css hack 是通过在css 样式中加入一些特殊的符号，让不同的浏览器识别不同的符号，已到达不同的css样式的目的。比如**.kwstu{width:300px;_width:200px;}**，一般浏览器会先给元素使用width:300px;的样式，紧接着后面还有个**_width:200px;由于下划线_width只有IE6可以识别，所以此样式在IE6中实际设置对象的宽度为200px，**后面的把前面的给覆盖了，而其他浏览器不识别_width不会执行_width:200px。**可以使用css hack解决部分兼容性问题**；
  
- 为什么不推荐使用CSS hack解决兼容性问题

 CSS hack是因为现有浏览器对标准的解析不同，为了兼容各浏览器，所采用的一种补救方法。CSS hack是一种类似**作弊**的手段，以欺骗浏览器的方式达到兼容的目的，是用浏览器的兼容性差异来解决浏览器的兼容性问题。因此，在设计之初，写CSS hack需要遵循以下三条原则：
1. 有效： 能够通过 Web 标准的验证
2. 只针对太古老的/不再开发的/已被抛弃的浏览器， 而不是目前的主流浏览器
3. 代码要丑陋。让人记住这是一个不得已而为之的 Hack, 时刻记住要想办法去掉它。现在很多hacks已经抛弃了最初的原则，而滥用hack会导致浏览器更新之后产生更多的兼容性问题。