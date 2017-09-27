
# 整理的关于css一些理解

   * css modules 是什么
   `css modules 是模块化css，也可以理解为vue的scope。它可以通过webpack打包生成一个hash值，这样就给css以及dom的class使用同一个hash值来分离css的作用域。:global是全局的:local是局部的。js导入styles从app.css中，然后给dom定义class，<div class='styles.blue'>i am color blue</div>。也可以使用compes来导入其他中css中的css。`
   * flex布局中的flex代表什么意义
   `flex是flex-grow flex-shrink flex-basis的缩写。flex:1；为数字时代表flex-grow；flex:2rem/20px；为width/height时代表flex-basis；flex: 1 2;代表flex-grow flex-shrink；flex:1 20px；代表flex-grow;flex-basis；`
   `flex-grow代表该元素在父元素中占据的大小比例。所有子元素会根据flex-grow来分配父元素的距离。flex-shrink代表元素的缩放比例。搭配flex-basis设置基本的宽高来进行分配缩放。flex-grow和flex-shrink都为不小于0的值有效。然后进行适当的增大缩小。`
   `order代表顺序，不根据soursecode的位置来排列元素。根据order的大小（可正可负）进行一个比较的过程。默认的为0；相等的按照sousecode的排列进行排列`
   * position有哪几种值，设置都有什么影响根据浮动
   `static,inherit,initial,absolute,realitive,fixed`
   `浮动不影响absolute，但影响static以及realitive。设置后realitive脱离文件原来的流，可理解为fload权重比realitive大。设置realitive仍旧可以设置margin,top,left来累加影响元素的位置，位置仍占据，但显示上会跟absolute一样可能挡住其他元素。`
   * div左右宽度各50%布局在ie6 ie7下出现问题
   `在于两个div中间存在空白节点，把空格去掉就行了。第二种方法是设置font-size为0；这个方法跟解决inline-block的间距一个道理。IE会把浮动的元素box认为inline-block（我认为，因为可以inline排列，又具有宽高）`
