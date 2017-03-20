---
title: 引用Iconfont做UI？设计师需要Care的那些事儿
subtitle:   " \"Something about svg\""
date: 2016-12-03 22:07:52
header-img: svg_bg.jpg
tags:
    - 开发对接
---


随着UI设计行业的发展，iconfont的概念也渐渐被大家熟知，今天就结合自己的工作经历，来聊聊设计师在使用iconfont做界面设计的时候，需要去care的一些问题。

<!--more-->

在说iconfont之前，有必要先来介绍一下SVG，SVG是个啥？我们来看看官方的定义：
> 
SVG(Scalable Vector Graphics，可伸缩性矢量图形)是由万维网联盟(W3C)推出的基于XML编码的开放式图形、图像标准。它虽然是一种二维矢量图形格式，但其中可以包含矢量图形、光栅图像及文本等。



      

   
就如官方定义中说的，矢量的！对于设计师而言，理解“矢量概念”的话，即：无限放大或者缩小都不会失真，非常的锐利清晰。如Illustrator & Sketch中的矢量图形，永远有着清晰的边缘。而在实际开发中使用SVG 的话，也是一样，图片可以始终保持着清晰状态，这相比于png或者jpg的优势是非常明显的。
__ 栗子还是要举一个的。__

![](http://upload-images.jianshu.io/upload_images/1338225-a8c2e716b9d46a68.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---
如图所示，同时用浏览器打开两张相同的图片，格式：左边是png；右边是svg

  ![](http://upload-images.jianshu.io/upload_images/1338225-ddeb1668f5d87161.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
---
乍一看，似乎差不多哎！OK，我们来放大到500%瞅瞅，如下图：
![](http://upload-images.jianshu.io/upload_images/1338225-bb65932819914a6e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

差别就出来了，png格式的图片已经开始模糊，而svg格式的，却依然保持着锐利清晰的边缘！

这就是svg的优势；---__ OK，那么iconfont又是啥？__ 简单说，就是将图标文字化处理；用展示文字的形式去展示图标，其本质是文字，而文字也是矢量的，无论放大或者缩小也不会失真；使用字体图标的好处：
__ 1.轻量性：__ 一个字体图标远比一个png或者jpg的图标要小。一旦字体图标加载了，就会马上被浏览器渲染出来，不需要下载一个图像。可以减少HTTP请求，还可以配合HTML5离线存储做性能优化。
__ 2.便利性：__ 字体图标可以通过font-size属性设置其大小，还可以加各种状态效果，包括normal、hover、disabled等状态；使用栅格图的话，必须得为每个不同的状态输出几个不同的图片资源。从根本上来说，iconfont和svg是不一样的，iconfont是字体，svg是图片，但是他们都具有“矢量特性”，关于两者的对比，后期会再做阐述；
---__ 今天我们主要还是来聊一下设计师层面，关于iconfont的使用：__



### 一．我们如何去设计一个iconfont；

OK，制作iconfont的话，我们还是得先输出svg格式，然后将其转化为iconfont；
  
一般在UI设计中，输出svg格式图片的话，大多使用Illustrator & Sketch，这里以sketch为栗，说明一下制作规则：__ 1.	一个svg中如果有两个及两个以上不同的形状，要使用布尔运算进行组合；__![](http://upload-images.jianshu.io/upload_images/1338225-3ebd55d43e496dad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
---
__2.	使用钢笔描边绘制的icon，在输出svg之前，需要将其转换为形状；形状也一定要是闭合的哦。__
![](http://upload-images.jianshu.io/upload_images/1338225-681e651cc03fcb97.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)__3.	在绘制完成之后，要给icon填充上颜色，建议以纯色为主（目前阿里iconfont也支持渐变色，多色块组合型icon，关于该类型，，后期再做讨论）__

![](http://upload-images.jianshu.io/upload_images/1338225-9b4c77ede407e390.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

__4.	很多iconfont的规范中会加入以下这么一条：一般建议以16x16的图标大小进行绘制（摘自iconfont绘制规则）。__这种设计规范考虑到了浏览器的一些因素。例：在PC上当图标小于等于16px时，或者复杂度高的图标会出现比较严重锯齿，部分浏览器中图标无法展示清晰，特别在chrome下的表现尤为严重。当然这并不是iconfont的错，而是浏览器本身的字体渲染机制决定的。16x16的这个规范可以说是以最小字号的情况去做设计，最小的字号都可以清晰，那么大字号的也一定会清晰，同时也可以确保了整体icon的统一性；但是实际工作中，这个规范同样也带来了一些不必要的工作量。譬如你在设计一个页面的时候，实际的UI画面中有一个32x50px的icon，如果我们先把它整体等比缩小，放置于16x16px的外框中（为确保统一感，一般icon不会贴边于外框）去排版输出，这个时候，本来这个iconfont的font－size值是50px（font－size值等于icon的高度，这点文章下一节会进行论证），但是因为我们已经给它套了一个外框，这个时候，设置50px的font－size，实际上50px作用的，是外框的高度，因此会导致里面icon实际显示出的高度，压根就没有达到50px。如果要解决这个问题，我们需要将16x16px的外框加上icon一起复制到原先的场景中，再去放大到原先icon的大小，量出外框的高度，再把这个高度给到开发…这个流程下来，我估计设计师，要疯…这是一个极其繁琐的过程，大大的增加了设计师的工作量。__总结：对于这个16x16px的规范设计要求，如果是基于设计一个系列的iconfont字体库的初衷，是极其合理的。但是实际工作开发场景中的话，这个规范，就会显得很鸡肋。__

---

### 二．视觉稿里面有了svg的icon，开发时我们如何做到精确还原；笔者这里以web设计为主，进行讨论：CSS是将每一个iconfont当作字体处理，可以设置字体的size值，从而来控制iconfont的大小。OK，那么问题来了，我做了一个iconfont以后，这个iconfont的“字体size”是多少？---
我们来做一个实验：我们在Sketch中绘制三个矩形，如图：
![](http://upload-images.jianshu.io/upload_images/1338225-f37737b024e012bc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
分别是正方形，瘦长型矩形，扁型矩形，把它们放在同一个iconfont的项目组里面。![](http://upload-images.jianshu.io/upload_images/1338225-3f72930a5aafbeb6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
---随后我们在实际开发中对这三个iconfont进行引用，并在CSS中设置它们三个的字体均是100px； 

![](http://upload-images.jianshu.io/upload_images/1338225-252f6379b36b174d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)---
同时展示三个icon：
![](http://upload-images.jianshu.io/upload_images/1338225-8b6d756fe656b56c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---OK，运行一下试试，我们看看结果：
![](http://upload-images.jianshu.io/upload_images/1338225-8e3bba056d35558f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
这个时候，是不是很一脸蒙蔽嘞？！怎么长得跟设计稿不一样呢？设置了一样的size值，为什么三张图片发生了这样的变化？仔细看一下，我们可以发现三张图的高度都是一致的，OK，我们把浏览器的截图导入ps，量一下：![](http://upload-images.jianshu.io/upload_images/1338225-86890e7b29f151a2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
我们不难发现，所有的图片的高度都是200px，也就是说，之前我们在代码里面设置的font－size是100px；实际上，在浏览器渲染的时候，是将100px当作图片高度处理的(因为笔者用的是Retina屏，所以实际是按照@2x渲染的，会有二倍关系)
> 
归纳：字体的数值，其实等于实际开发中图片的高度。**那么又有了一个新的问题，对于各种各样的场景，我们如何做到统一呢？**
譬如下方这样的列表
![](http://upload-images.jianshu.io/upload_images/1338225-93e2650d4a9303ac.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
左侧的icon其实每一个高度都是不一致的，难道每一个icon都要去设置一个高度？对于开发而言，简直太麻烦啦。那么该如何处理呢？当我们在实际导出iconfont切图的时候，可以使用切片工具，去给每一个icon套上一个正方形的“外框”，这样导出的icon，实际的字体size大小，就是正方形的边长。![](http://upload-images.jianshu.io/upload_images/1338225-1c899728a8d5bce8.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](http://upload-images.jianshu.io/upload_images/1338225-99160e3b4fc3e270.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
---OK，输出iconfont，在代码中引用新的icon，我们来在实际应用中看一下效果
![](http://upload-images.jianshu.io/upload_images/1338225-07c856a97521ca16.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

和视觉稿一样，精确的还原啦！那么，对于上面例举的设置页面，也可以使用同样的方法去还原设计稿。
对于该设置页面，我们需要提供给工程师一组尺寸一样的iconfont切图，并且告诉他们这些iconfont都使用一个font－size值，针对这些icon，工程师可以写一个公用的class类；如果需要调整大小的话，只需要改变这一个数值，就可以改变所有icon的大小，是不是很方便嘞！
**因此：站在UI的角度，我们需要做到的是同一模块icon的统一性（譬如刚刚的设置页面）。而对于其他场景的不同页面，当所有icon的方形外框调整为一个宽高的时候，没有必要确保里面icon给人视觉比重一致。**

---### 三．关于浏览器兼容性的问题，在使用iconfont时候需要注意的。正如文章开头所提到的，在16px的时候，iconfont会开始变得不清晰，但根据笔者和前端工程师的工作（撕逼）经验来看的话，一般在16px的时候，还是可以识别，失真度并没有那么糟糕。
但是在大部分浏览器中，当字体小于12号字的时，浏览器渲染的时候，会出现兼容性的问题。目前的话，针对于这个问题，是有前端解决方案的，但是会增加工程师的工作量！
那么设计师在处理这类的iconfont的时候，可以对于该类较小的icon，以12px的“方形边框切出”（手机端的页面，如果是使用@2x做设计的话，需要以24px宽高处理方形外框），这样开发可以以12号字去处理，避免了很多web兼容性问题，同时也减少了工程师的工作量。![](http://upload-images.jianshu.io/upload_images/1338225-79021ed099d8a0cd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
同时，在处理该icon与其他元素之间的距离的时候，以方形边框为边界，去标注方形边框到其他元素之间的距离，给到工程师。以上是和我司前端阮文小涛涛合作（撕逼）过程中，总结出来的一些点，哈哈，非常感谢他！希望这些经验可以对各位刚使用svg做设计的UI有帮助。啊哈！不知道不觉已经深夜啦！就码到这吧～晚安咯～
***![](http://upload-images.jianshu.io/upload_images/1338225-3ec7bd8fc3aba509.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





