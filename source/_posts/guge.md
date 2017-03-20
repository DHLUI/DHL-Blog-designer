---
title: 精读Material Design设计规范之「谷歌Style篇」
subtitle:   " \"Let's talk about the style of Material Design\""
date: 2017-01-30 16:28:14
header-img: guge_bg.jpg
tags:
    - 视觉设计
---

> 谷歌设计规范基本上可以视为设计规范的范本，而且不仅仅是在UI层面，甚至可以说是传统设计的进化范本。考虑到规范较为庞大，所以本文仅针对Style（风格）部分做精读。

先来看一下谷歌官方的定义：

> A visual language for our users that synthesizes the classic principles of good design with the innovation and possibility of technology and science. 

MD design是啥呢？简单来说，就是将科学、技术、创意等等综合到一起，总结成一套规则，形成一个视觉语言。关于全面的官方文档，可以点击这里[MD design官方设计规范](http://www.google.com/design/spec/material-design/)（需要翻墙哦～）。如果没有翻墙的朋友，可以[查看这个不需翻墙版本](http://blog.chengyunfeng.com/design/spec/material-design/introduction.html)（一个基于SAE托管的独立博客，作者已将MD规范整体Fork）

### 一.颜色概述(Color)

在官方文档中，是这样描述 MD的颜色的：
> Color in material design is inspired by bold hues juxtaposed with muted environments,deep shadows，and bright highlights.

这里着重提到了几个关键词：

* hue——色彩
* environments——环境
* shadows——阴影
* highlights——高光

我们可以从字面上去理解：通过大胆的色调，强烈的阴影和高光与周边环境来渲染颜色。但是呢，这里在信息传递层面，也有另外一重寓意：highlights表明的是界面中需要强调的部分，shadows代表的是信息的层级，environments环境是文本信息周边的信息颜色；这是从信息层级的角度去理解color的意义。

下面我们来看一下MD规范中推荐的__ UI调色板：__ 

纯红色、粉红色、纯紫色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-1-1.png)

深紫色、藏青色、纯蓝色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-2-2.png)

浅蓝色、天青色、水鸭色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-3-3.png)

绿色、亮绿色、柠檬绿：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-4-4.png)

黄色、棕黄色、橙色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-5-5.png)

深橙色、褐色、灰色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-6-6.png)

蓝灰色、黑白色：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-7-7.png)

这些颜色，我们大致上可以分为两个类别，我们不难发现：从开头的第一个纯红色（Red）到深橙色（Deep Orange），正好是色轮的一圈：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-8.png)

在谷歌推荐的调色板中，也单独列出了另外四个特殊的颜色：褐色、蓝灰色、灰色、黑白。

在每一个画板中，会有两个模块，我们以纯红色举例：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-1-1-1%EF%BC%8D1.png)

上方的称之为标准色，纯红色的基准是“500”的饱和度；标准色中的其他颜色，做饱和度的加大或者削弱产生；下方的颜色则称之为推荐色；

**关于标准色和推荐色的使用方法，我们来以谷歌规范中的视频样本作阐述：**
*这里是视频的地址链接：[点击查看谷歌官方配色视频](http://v.youku.com/v_show/id_XMTMyODk3NjIwNA==.html)（考虑到部分同学无法翻墙，在这里提供一个优酷链接）*

我们来根据视频的过程，学习一下谷歌推荐的配色方法：
![](http://oi68vw4nk.bkt.clouddn.com/palette-41.png)
注意这个色板，下面我们开始取色：

其中的一个颜色放大之后展开，变成了九个颜色方格：
![](http://oi68vw4nk.bkt.clouddn.com/palette-42.png)
这个画面是不是很眼熟呢？这九个板块，对应的就是刚刚色板中的饱和度100-900的颜色。

现在我们开始在标准色色板中移动（饱和度均为500），OK，我们选中了一个蓝色，这个时候呢，在右侧的界面中，就填充进了我们所选择的主色。
![](http://oi68vw4nk.bkt.clouddn.com/palette-43.png)

这个时候，左侧的图变成了基于刚选择的蓝色生成了蓝色标准色色板，一共从100-900，有九个不同的饱和度：

![](http://oi68vw4nk.bkt.clouddn.com/palette-44.png)

下面开始进行辅色的搭配：

我们从左侧的色板中，选择了饱和度为700的蓝色，其余部分上色，如图：
![](http://oi68vw4nk.bkt.clouddn.com/palette-45.png)

随后我们对按钮等控件进行着色，这也是color定义中的“bright highlights”
![](http://oi68vw4nk.bkt.clouddn.com/palette-46.png)

我们来归纳一下这整个着色过程：以标准色为界面的主色调；再以标准色做上下抖动（±200至±300的饱和度差），选了一个颜色，做导航色；最后从推荐色（A色值）选择一个颜色，作为可点击颜色。当然，还有一个颜色，就是灰色，用于界面的背景色。

这个视频简述了谷歌规范配色的指导思想，也是非常的学院派做法——`它认为颜色是带有层级的、包含着逻辑含义的，而不是随便使用的。`

还记得这个视频开头的那句话吗？"There no wrong colors."从来没有错误的颜色；颜色的使用好坏，需要去看如何搭配。人类对于颜色的感知是非常主观的，比如你说橙色代表着热情，但这也只是绝大部分人对于橙色的感觉；可能会有人觉得橙色是“静谧”，这个是没有对错的，只是大家对于颜色层面感性理解的角度不一样。但是于颜色的信息层级而言，则是相对理性和富有逻辑的。这点也是谷歌规范在界面配色里的中心指导思想。

### 二.在颜色层面，谷歌和苹果设计风格的对比（Apple & Google）

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-39.png)

谷歌的视觉规范&和苹果设计风格，可以说是完全不同的两个不同的类型，为什么这么说呢？

MD设计规范着重诠释了大胆而具有强烈对比性的色彩，它认为这个世界应该是多姿多彩的；鲜艳富有个性的色彩可以使用户保持愉悦的心情。并且设计基本理念中，谷歌是把界面视为纸张，用“纸张”去传递信息，可以说谷歌的工程师可以说是**文艺派的！**

而在苹果设计规范中呢？苹果规范对颜色提到的信息却不多，苹果认为你用亮色，用暗色是开发者自己家产品的事情，在iOS系统规范中没有必要做太多的限制；**苹果认为凸显内容、传递信息才是核心。**谷歌相对苹果比较“激进”；苹果相对谷歌比较“保守”。对于用户的理解也不一样，谷歌希望让用户有印象深刻的体验，让用户感觉到“艺术”，通过大胆的颜色打动用户的心。而苹果则认为，真正优秀的设计，应该是潜入你的生活中且不着痕迹的，用户不需要记住我的颜色，我们只需要帮助用户顺畅的完成用户目标即可。

### 三.颜色主题（Color Schemes）的应用

下面，谷歌在文档中举了一个例子，来说明如何配色，也就是如何运用颜色为产品定义颜色主题，官方文档中，颜色主题一共包括三个方面：

* primary color——主色调
* secondary color——次级颜色
* accent color——重点色（可交互区域）

我们来看一下文档中的截图：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-22.png)

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-24.png)
*上方的两张图为界面的截图，下方的为界面使用的颜色色板*

界面中使用的主色调为藏青色（indigo）500的饱和度，对应的为导航栏；次级颜色为700饱和度的藏青色——状态栏；而重点色使用了（pink）——A200，也就是非常明显的收藏按钮。这个例子简单的说明了主色、次级颜色、重点色的使用方法（其实也就是视频中配色demo的进一步诠释）

**主色的多样性：**

> **Primary color variations：**

> Another alternative accent color is the 500 version of your primary color on white backgrounds.However, if your background color is already the 500 version of your primary color, make your accent color either white 100% or black 54%.

这句话简单的定义了“可交互区域”颜色的特点：在白色背景下，可交互区域的颜色色值是500饱和度的主色；但是呢，如果背景区域已经是500饱和度的主色了，那么可交互的信息颜色就要调整为：alpha＝100%的纯白 or  alpha＝54%的纯黑。

举个例子：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-25.png)

上图中的文字按钮，就是在白色的背景上，其样式需要使用主色；而如果其背景本身就已经是主色了，则可交互信息需要使用纯白或者54%的黑色：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-26.png)


由此可见，在谷歌规范中，其实并不存在标准意义上的灰色，所有的灰色都是由黑色加上透明度而来；对于主色上的白色也一样，也是做透明度的变化形成。在规范文档中，也给出了如下的解释：

> 
**Use opacity instead of grey：**

>  Black or white text that is transparent remains legible and vibrant against background color changes. This makes it more flexible than grey text in the same contexts.

谷歌认为使用透明度去约束文字的颜色，会更加的灵活，为什么这么说呢？笔者举个例子：

我们现在app中有两个按钮，这两个按钮的背景色都是“500 version of your primary color ”，但是呢，颜色的色相不一样，一个是红色，一个是蓝色；

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-29.png)

如图所示，上面是两个按钮在disabled的情况下的颜色，okay，如果我们直接用颜色标记两个按钮disabled状态下的文本颜色，则左边的按钮为：#90CAF9；右侧的按钮为：#F9A19A；这是两个不同的色值，这个时候，如果我的按钮背景色更换，则我们也需要去同时更换文本在disabled状态下的颜色，非常的麻烦。

我们来看一下使用透明度标记的方法：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-30.png)

如图，极其的方便，对于不同场景的按钮，我只需要写一个颜色：#ffffff alpha＝50%即可，如果我需要更改这个disabled的颜色，我只需要在颜色库里面统一更新这个颜色即可。并且这样做的话，可以把背景色透一点出来，使文本颜色不那么死板。

同样的，谷歌规范也为我们定义了在浅色背景和深色背景上的文本用色：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-27.png)

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-31.png)

这里以浅色底、深色文本的例子来说明：
* 主文本（primary text）：纯黑 opcity＝87%
* 次级文本（secondary text）：纯黑 opcity＝54%
* 不可点击／暗示说明文本（disabled／hint text）：纯黑 opcity＝38%
* 主色和点击色在浅色文本上则是100%


### 四.关于阴影（Shadow）

有位UI设计师朋友之前和笔者聊MD的时候，发现了一个“神奇”的现象：我们在谷歌官方的sketch模板文件中，发现了卡片式的投影，其实有“两层”：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-32.png)

好像有点奇怪，仅仅是一个卡片的阴影而已，有必要去做两层吗？我们来看一下官方的解释：

![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-33.png)

“Combined shadow from key and ambient lights”——这里有两层阴影，一层是环境光投射的阴影，另一层是关键光照射在material卡片上投射的阴影。这是谷歌给出的解释。

下面我们再来看一下真实的物理环境中，阴影的黑度和扩散距离的关系：

一般来说，随着距离的原来越远，阴影的黑度也越来越小，并且这种变化呈减速曲线（一开始变化的快，之后越来越慢）
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-34.png)

说到这里，理论上我们只需要让开发把阴影处理为这种曲线变化的模式即可。可惜的是，在实际的手机中，阴影的黑度和扩散距离一般呈线性变化（非曲线），因为手机处理器性能问题, 实时计算平滑为曲线后的阴影会导致可怕的耗电与发热，所以谷歌只能在这方面妥协，将阴影曲线拉直。那么谷歌该如何去模拟真实环境中的阴影效果呢？我们来做一下拆分：

首先是一层环境光的投影，这种投影时极其微弱的。
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-35.png)

随后，还有一层光——关键光源照射产生的阴影，比如日光、灯光等，产生的阴影比较急促：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-36.png)

那么如果我们将两者柔和呢？
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-37.png)

这个时候我们就可以得到这样一种视觉感知：
![](http://oi68vw4nk.bkt.clouddn.com/style-color-palette-38.png)

近似的可以形成一个“曲线”，从而规避了手机将阴影曲线拉直的问题。同样，这也是我们平时在做banner或者插画的时候，一般会去做两层投影的原因——为了模拟真实环境中的阴影效果。所以某种意义上来说，这也刚好和谷歌官方定义中的“key and ambient lights”不谋而合。


### 五.谷歌图标（Icon）

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon08.png)

先来看一下官方的定义：

>Icons

>Material icons use geometric shapes to visually represent core ideas, capabilities, or topics.

材料设计的icon是几何形的，并且能够很好的表达出核心主题、功能意义、话题。主题和话题有啥区别呢？主题（core ideas）就是最核心的定义，一句话可以描述清楚的，比如咱们说UI中国，它的logo很简单——“UI”两个字母；它的核心就是告诉用户，我这个网站是关于UI的。那话题呢？话题（topics）是一个大主题下面的一个话题，两者有“父子关系”。

__关于产品图标和系统图标：__

> __Product icons__ are the visual expression of a brand’s products, services, and tools.

> __System icons__ represent a command, file, device, directory, or common actions.

产品图标可以简单的理解为自己家产品自有的，代表着自己家产品品牌的；而系统图标则是用于整个安卓系统的，比如安卓L中的聊天气泡。

同时，谷歌规范中也规定了icon的尺寸：

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon01.png)



关于dp，可以详见笔者之前的一篇文章[设计师需要了解的一些移动端适配原理](http://daihanlin.cn/2017/01/02/%E2%80%9Cppi%E2%80%9D/)

在上图中提到的表格中，谷歌也为我们定义了浅色底和深色底的icon使用样式：

* 浅色底可用——opacity＝54%
* 浅色底不可用——opacity＝26%
* 深色底可用——opacity＝100%
* 深色底不可用——opacity＝30%

这些样式也和上篇文章中提到的文本的使用规则类似——谷歌规范建议使用透明度去变化图标的normal、pressed、disabled等状态。

下面我们来看一下图标制作规范：

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon02.png)

这是谷歌图标的制作规范，大家是不是觉得很熟悉？在iOS规范里面，也有一个这样的制作规范：

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon03.png)

但是谷歌的图标规范可以说和iOS是完全不一样的；谷歌通过Keylines去约束图标，那么该怎么去理解Keylines呢？我们看下图

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon04.png)

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon05.png)

不难发现，keylines框选出了几种形状：正方形、圆形、瘦矩形、扁矩形。对于不同形状的icon，使用了keylines确保了其“视觉重量”一致。说到这可能部分同学还会有点懵，我们来打一个比方，上图中的蓝色区域就是一块橡皮泥，我们用手捏橡皮泥的时候，可以把它做成原型，方形，矩形；但是对于这些形状来说，其面积大小是一定的；这也就是keylines的作用——确保所有icon的“视觉重量”一致。

### 六.图片使用规则（Imagery）

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon06.png)

在官方推荐的图片使用规则中，建议使用摄影照片或者插画作为图片素材；一般对于实物，首先建议以摄影的方式来表现，其次才是插画模式。

![](http://oi68vw4nk.bkt.clouddn.com/gugeicon07.png)

在使用的图片中如果需要加上文字的话，则需要加上一个mask（遮罩），来确保文字的可读性；这个遮罩可以使仅仅覆盖在文字特定区域来凸显文字；也可以是覆盖整个图片，这个可以由设计师选择；

**关于图片动效的几种表达方法：**

在图片载入的时候，一般有以下几种动效模式：

* 透明度从无到有
* 伽马值（gamma）的变化，可以简单的理解为从黑到白
* 饱和度的变化，可以理解为从黑白到彩色

当然，在实际的动效场景中，可以是使用其中的一种模式变化，也可以是三种效果同时进行。这样可以让图片出现的过程更加的细腻。


### 七.总结（Summary）

MD可以说是一套极其全面的视觉规范，乃至可以说是一种视觉语言，几乎所有细节它都已经为我定义了视觉方案。但笔者认为：规范仅仅提供的是指导意见，设计师、工程师没有必要完全照搬照抄。针对自己的用户、业务，我们需要做更加符合我们“产品特质”的设计方案。如果仅仅是为了符合规范去设计，忽略了产品本身，那就本末倒置了。所以笔者认为对于设计师而言，MD规范是一个“**参考答案**”，而非“**标准答案**”。


***  

*本文主要讨论的是MD风格（style）部分，文中也把一些和style模块耦合的其他模块拿过来做了整理；文中仅针对规范要点做了分享（部分过于学院派难以落地的理论并未讨论），有兴趣的同学可以全面的研究一下MD官方文档，谢谢。*







