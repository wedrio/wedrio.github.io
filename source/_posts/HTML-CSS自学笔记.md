---
title: HTML+CSS自学笔记
date: 2020-05-14 11:34:16
tags:
---
前面空了一部分没有做笔记，太懒了，后面补出来。
## strong与b、em与i？  
表现形态都是文本加粗和斜体  
strong和em是具备语义化的，而b和i是不具备语义化的。
<!--more-->
## 引用标签
blockquote：引用大段的段落解释  
q：引用小段的短语解释  
abbr：缩写或首字母缩略词  
address：引用文档地址信息  
cite：引用著作的标题   

## iframe嵌套页面
iframe元素会创建包含另外一个文档的内联框架（即行内框架）。  
也就是在一个页面中可以嵌入另外一个页面  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/html+css_zs10.jpg.png)
应用场景：数据传输、共享代码、局部刷新、第三方介入。  

## br与wbr
br换行、wbr软换行  

## pre与code
针对网页中的程序代码的显示效果  
## map与area
给特殊图形添加链接，area能添加的热区图形有：矩形，圆形，多边形  

## embed与object
嵌入一些多媒体，如flash动画、插件等，区别是兼容性  

## audio与video（H5的功能）
Audio嵌入音频文件  
Video嵌入视频文件  
默认控件不显示，可通过controls属性来显示控件。  
Source备选方案，看网页是否支持格式  

## 文字注解与文字方向
Ruby标签定义ruby注释（中文注音或字符），rt标签定义字符（中文注音或字符）的解释或发音。  
Bdo文字反向

## 扩展link标签
可以引入顶部标签小图标
## 扩展meta标签
Meta添加一些辅助信息

## html5新语义化标签（常用）
header 页眉  
footer  页脚  
main  主体  
hgroup  标题组合  
nav  导航  
article  独立的内容  
aside 辅助信息的内容  
section  区域  
figure  描述图像或视频  
figcaption 描述图像或视频的标题部分  
datalist  选项列表  
details/summary  文档细节/文档标题  
progress/meter  定义进度条/定义度量范围  
time  定义日期或时间  
mark 带有记号的文本  

## 表格扩展
添加单线： border-collapse：collapse  
隐藏空单元  empty-cells：hide  
斜线分类  border/rotate  
列分组  colgroup/col  
## 表单控件扩展
美化表单控件 ：label+:checked    position+opacity
## 新的input控件
email：电子邮件地址输入框  
url：网址  
number：数值  
range：滑动条  
date、month、week：日期控件  
search：搜索框  
color：颜色控件  
tel：电话号码输入框（在移动端默认数字键盘）  
time：日期控件

## 新的表单属性 
autocomplete：自动完成 默认 on/off  
autofocus：获取焦点  
required：不能为空  
pattern：正则验证

## 数据传递
method：数据传递方式  
enctype：数据传输类型  
name/value：数据的键值对
## 表单扩展
扩展标签  
fieldset：表单内元素分组  
legend：为fieldset元素定义标题  
optgroup：定义选项组
	
## BFC规范
触发BFC规范的元素，可以形成一个独立的容器。不受到外界的影响，从而解决一些布局问题。  
触发样式：float、position、overflow  
解决margin叠加问题  
解决margin传递问题  
解决浮动问题  
解决覆盖问题







## 浏览器前缀
 ![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/iframe.jpg.png)
## transition过渡
transition-property：规定设置过渡效果的CSS属性的名称。  
transition-duration：规定完成过渡效果需要多少秒或毫秒。  
transition-delay：定义过渡效果何时开始。  
transition-timing-function：规定速度效果的速度曲线。
		
## transform变形
translate：位移  
translateX  
translateY  
translateZ（3d）  
scale：缩放（值是一个比例值，正常大小就是1，会以当前元素中心点进行缩放）  
   scaleX  
   scaleY  
   scaleZ（3d）

## rotate：旋转（旋转的值，单位是角度deg）
rotateX（3d）  
rotateY（3d）  
rotateZ（等价于rotate，正-顺时针）  
skew：斜切  
   skewX：单位也是角度，正值向左倾斜  
   skewY
## transform变形
注意事项：  
	1.变形操作不会影响其他元素。  
	2.变形操作只能添加给块元素  
	3.复合写法，可以同时添加多个变形操作  
执行时有顺序的，先执行后面的操作，再执行前面的操作。  
translate会受到rotate、scale、skew的影响  
	4.transform-origin变形的基点位置：x y z（3d）
## 利用斜切和overflow做斜切导航。
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/xieqienav.png)
## 变形的列表
主要是利用rotate旋转加上overflow和hover做 特殊效果

## animation动画
animation-name:设置动画的名字（自定义）  
animation-duration：动画的持续时间  
animation-delay：动画的延迟时间  
animation-iteration-count:动画的重复次数，默认值为1，infinite无限次  
animation-timing-function：动画的运动形式  
注：  
	1.运动结束后，默认停留在初始位置  
	2.@keyframes ：from->0% ,to->100%  
animation-fill-mode：规定动画播放之前或之后，其动画效果是否可见。
none（默认值）：在运动结束之后回到初始位置，在延迟的情况下，让
0%在延迟后生效  
backwards：在延迟的情况下，让0%在延迟前生效  
forwards：在运动结束的之后，停到结束位置  
both：backwards和forwards同时生效  
animation-direction：属性定义是否应该轮流反向播放动画。  
alternate:一次正向(0%-100%),一次反向(100%-0%)。  
reverse:永远都是反向,从100%-6%。   
normal(默认值):永远都是正向,从0%-100%  
## 动画切换图标
利用关键帧实现效果
## loading加载效果
创建4个div然后再创建4个  
圆角50%，将其中4个div旋转45deg  
添加动画
## animate.css
一款强大的预设css3动画库。  
官网地址：<http://daneden.github.io/animate.css/>  
基本使用：  
animated:基类（基础的样式，每个动画效果都需要加）  
infinite:动画的无限次数
## transform3D相关属性
rotateX（）：正值向上翻转  
rotateY（）：正值向右翻转  
translateZ（）：正值向前，负值向后  
scaleZ（）：立体元素的厚度  
3d相关属性  
perspective：离屏幕多远的距离去观察元素，值越大幅度越小。  
perspective-origin：景深-基点位置，观察元素的角度。  
transform-origin: x y z   
transform-style：3D空间  
flat（默认值2d），preserve-3d（3d，产生一个三维空间）  
backface-visibility：背面隐藏  
hidden，visible（默认值）  
3d写法  
scale3d（）：x y z  
translate3d（）：x y z  
rotate3d（）：四个值 0|1(x轴是否添加旋转角度) 0|1(y轴是否添加旋转角度)  
0|1(z轴是否添加旋转角度)  deg
## 立方体制作
transform-origin：center center 数值（Z轴只支持数值）
		

## 旋转相册
6张图片重叠，两两旋转不同方向60deg，然后在沿着z轴平移  
然后添加一个旋转360deg的效果

## 背景扩展
background-size：背景图的尺寸大小  
cover：覆盖  
contain：包含  
background-origin：背景图的填充位置  
padding-box（默认）  
border-box  
content-box  
background-clip：背景图的裁切方式  
padding-box  
border-box（默认）  
content-box  
注：复合样式的时候，第一个是位置，第二个是裁切。

## css3渐变
1，线性渐变-> linear-gradient是值，需要添加到background-image属性上注：渐变的0度是在页面在下边，正值会按照顺时针旋转，负值按逆时针旋转。  
2，径向渐变-> radial-gradient


## @font-face字体图标
font-face是Css3中的一个模块，他主要是把自己定义的web字体嵌入到你的网页中。  
好处：  
1，可以非常方便的改变大小（font-size）和颜色（color）  
2.放大后不会失真  
3，减少请求次数和提高加载速度  
4.简化网页布局  
5，减少设计师和前端工程师的工作量  
6，可使用计算机没有提供的字体  
使用：@font-face语法  
.woff等文件都是做网页兼容处理的  

## iconfont-阿里巴巴矢量图库
<https://www.iconfont.cn/>
## 自定义字体图标
创建svg文件  
上传IcoMoon-Free

## 文字阴影
text-shadow：  
x y blur color 多阴影  
注：阴影的默认颜色跟文字一样 通过逗号的方式进行分割，可以设置多阴影

## 盒子阴影
box-shadow：  
x y blur spread color inset outset  
注：默认阴影为黑色 默认为外阴影 多阴影用逗号分割


## mask遮罩
url   repeat   x   y   w   h  
注：mask目前还没有标准化，所以需要加前缀

## 倒影
box-reflect  
above  below   left   right  距离   遮罩 | 渐变  
注：scale（-1）翻转

## blur模糊与calc计算
filter：blur()  
calc计算：  
四则运算 例如：一个盒子无论父容器怎么扩大就想宽度小100px  
那么就可以用width:calc(100% - 100px)

## column分栏布局
column-count：分栏的个数  
column-width：分栏的宽度  
column-gap：分栏的间距  
column-rule：分栏的边线  
column-span：合并分栏（主要针对标题）  
注：分栏宽度和个数冲突

## 伪元素概念与意义
伪类与伪元素  
在CSS2.1中对伪类和伪元素的区别比较模糊。CSS3中对这两个概念做了相对较清晰地解释，并且在语法上也做了很明显的区分。  
CSS3中规定伪类由一个冒号开始，然后为伪类的名称；伪元素由两个冒号开始，然后为伪元素的名称。  
伪元素概念  
伪元素本质上市创建了一个有内容的虚拟容器。这个容器不包含任何DOM元素，但是可以包含内容。另外，开发者还可以为伪类元素定制样式。  
::selection  
::first-line / first-letter  
::before / after  
…

## hack概念与css属性前缀法
CSS Hack用来解决浏览器的兼容性问题，为不同版本的浏览器定制编写不同的CSS效果，使用每个浏览器单独识别的样式代码，控制浏览器的显示样式。  
Hack分类  
1.CSS属性前缀法  
属性前缀法是在CSS样式属性名前加上一些只有特定浏览器才能识别的hack前缀，以达到预期的页面展现效果。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/cssSXQianZhui.png)
2.选择器前缀法  
选择器前缀法师针对一些页面表现不一致或者需要特殊对待的浏览器，在css选择器前加上一些只有某些特定浏览器才能识别的前缀进行hack。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/XZQQianZhui.png)
3.IE条件注释法  
这种方式是ie浏览器专有的hack方式，微软官方推荐使用的hack方式。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/IETiaoJian.png)

## ie低版本常见bug
常见兼容问题：  
	1.透明度ie8以下不识别 解决filter:alpha(opacity=50)(ie6不行)  
	2.双边距 ie6同时设置了浮动和margin 解决方法   _display:inline  
	3.最小高度 ie6下最小高度为19px 解决方法：overflow：hidden  
	4.图片边框 ie10以下 解决办法 border：none  
## 渐进增强与优雅降级
渐进增强：针对低版本浏览器进行构建页面，保证达到最基本功能，然后再针对改机浏览器进行效果、交互等改进和追加功能达到更好的用户体验。  
优雅降级：一开始就构建完整的功能，然后再针对低版本浏览器进行兼容。

## 等高布局
magin-bottom负值和padding-bottom正值实现  
利用父容器的voerflow:hidden溢出隐藏  
## 双飞翼布局(三列布局)：左右固定，中间自适应
1.BFC规范  
2.定位  
3.浮动（利用magin-left负值实现）  
4.flex弹性
## flex弹性布局
随着移动互联网的发展，对于网页布局来说要求越来越高，而传统的布局方案对于实现特殊布局非常不方便，比如垂直居中。  
2009年，W3C提出了一种新的方案-Flex布局，可以简便、完整、响应式地实现各种页面布局。目前，它已经得到了所有浏览器的支持，这意味着，现在就能很安全地使用这项功能。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flex1.png)
flex-direction  
控制子项整体布局方向，从左往右、从右往左、从上往下、从下往上。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flexa1.png)
flex-wrap  
控制子项整体单行显示还是换行显示  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flexb2.png)
flex-flow  
是flex-direction和flex-wrap的缩写，表示flex布局的flow流动特性。第一个值表示方向，第二个值表示换行，中间用空格隔开。  
justify-content  
属性决定了主轴方向上子项的对齐和分布方式。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flex4.png)
align-items  
items指的就是flex子项们，因此align-items指的就是flex子项们相对于flex容器在侧轴方向上的对齐方式。  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flex5.png)
align-content  
可以看成和justify-content是相似且对立的属性，如果所有flex子项只有一行，则align-content属性是没有任何效果的。   
作用在flex子项上的CSS属性  
![](https://cdn.jsdelivr.net/gh/wedrio/ImageHosting/wedrio-pic/flex6.png)
