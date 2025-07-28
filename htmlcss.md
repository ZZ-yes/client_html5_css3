### Day1

- 现在的主流软件都是C/S架构，C是客户端，S是服务器

·用户通过客户端来使用软件

·服务器为用户提供各种服务器



- 客户端的呈现形式：

1.传统的图形化界面的客户端，如office、qq、王者荣耀、和平精英

 特点：需要安装、跨平台性差，导致开发成本高

2.以网页为界面的客户端（B/S架构，B是browser），如京东、淘宝、知乎

 特点：无需安装，跨平台性好，开发成本低



#### 网页的概述

- 伯纳斯李是万维网的发明者

- 网页需要运行到浏览器中

- 网景公司、微软公司、当时比较大的浏览器厂商，生产浏览器的公司，为了竞争市场份额开始了第一次浏览器大战，最终微软的IE浏览器取得了胜利

- 由于浏览器之间的恶性竞争，引发了网页的兼容问题，同样一个网页在不同的浏览器中显示效果不同

- 为了解决这个问题，伯纳斯李创建了W3C（万维网联盟）专门负责指定万维网中的各种标准

- 由于在第二次浏览器大战中，Google公司的chrome取得绝对的胜利，所以现在开发中几乎不再考虑兼容问题了

- 根据W3C的规范，一个网页被分成了三个部分：

  1.结构、表现和行为

  结构：网页的结构，网页中哪里是标题、哪里是图片、哪里是链接

  HTML负责定义网页的结构

  表现：网页的外在样式，网页的颜色、网页的布局

  CSS负责网页的表现

  行为：网页和用户的交互行为

  JavaScript负责网页的行为



#### HTML

- HTML负责定义网页的结构

- HTML全称Hyper Text Markup Language（超文本标记语言）

  文本：在计算机中使用纯文本编辑器编写的内容被称为文本

  word编写的内容不是纯文本，而是富文本（纯文本，只有文字，和基本的标点。

富文本，可以有图，可以有各种特殊标点，分段等格式。）

- 网页的扩展名是.html，一个网页最终由浏览器渲染呈现

- 标记：标记用来告诉浏览器中网页中不同的内容

- 在网页中使用html标签作为标记，来标记不同的内容

   HTML标签，成对出现，<标签名>标签体</标签名>

- HTML就是通过不同的标签来识别出网页中的不同内容，学习HTML就是学习各种标签



网页的基本结构：

```html
<!DOCTYPE html> 
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```



<!DOCTYPE html> 
文档声明，用来声明当前网页的版本，这个用来表示当前网页是遵循HTML5规范的
doc指Document，表示文档，文档就是网页，一个网页就是一个文档
type指类型
- html
  html根标签，一个网页有且只有一个根标签，其他标签都应该在根标签的内部

- head

html的子标签（子元素）

head表示网页的头部，可以在head中设置网页的各种数据，head中的内容不会在网页中直接显示

- meta，head的子元素，用来设置网页的元数据

  charset="UTF-8" 属性名=属性值，主要用来避免乱码问题

  title，head的子元素，用来设置网页的标题，会显示在标签上

- body

html的子标签，网页中所有的元素应写在body中



注释 ，注释不能进行嵌套！

1.<!---->

2.ctrl+/



#### 标签

title表示标题标签，文字会显示到标签页上

  搜素引擎在抓取页面中，会通过title的内容来识别网页的主要内容

  这部分是SEO相关知识（SEO搜索引擎优化）



HTML标签，一个标签也被称为一个元素

   成对出现，<标签名>标签体</标签名>

   自结束标签：1.<标签名> 2.<标签名 />

  

   属性：在开始标签（或自结束标签）中可以为元素设置属性，

   属性用来描述元素，属性是一个名值对结构，属性名="属性值"

  一个元素可以同时指定多个属性，多个属性之间使用空格隔开

  有些属性，属性名与属性值相同，此时可以省略属性值  

  html中不区分大小写，但是建议用小写



 标签列表：

  https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Elements

列表之间可以相互嵌套

  列表

​    有序列表

​    \- 使用ol创建有序列表

​    \- 在ol中使用li来表示列表项



​    无序列表

​    \- 使用ul创建无序列表

​    \- 在ul中使用li来表示列表项



​    定义列表

​    \- 使用dl创建定义列表

​    \- 使用dt来定义被描述的内容

​    \- 使用dd来对内容进行描述

#### 语义化标签

网页除了需要被人看之外，还需要爬虫程序爬取

   W3C就希望能够帮助程序更好的爬取这个页面

   于是他就添加了很多不同的语义化标签来帮助程序识别页面



   mian  主要内容，一个页面中最好只有一个main标签

   header 头部内容，可以多个

   footer 底部内容，可以多个

   article 表示独立内容

   aside 侧边栏，和主体独立的内容

   nav 表示导航

   section 独立的区块

  通过这些语义化标签，可以对网页中的不同内容进行描述，

  方便爬虫程序识别网页，但是大部分情况下我们不会大量使用这些标签

#### 元素间的关系

标签 tag

  元素 element



  元素之间的关系：

  父元素

  \- 直接包含子元素的元素是父元素

  子元素

  \- 直接被父元素包含的元素



  祖先元素

  \- 直接或间接包含后代元素的元素是祖先元素

  \- 父元素也是祖先元素

  后代元素

  \- 直接或间接被祖先元素包含的元素是后代元素

  \- 子元素也是后代元素



  兄弟元素

  \- 拥有相同的父元素

#### 超链接

使用a标签来定义一个超链接

  通过超链接可以跳转到其他的页面



  属性：

  href：指定要跳转的位置，需要一个路径作为参数 

  target：指定页面打开的位置

  可选值：

​    _self 默认值，在当前页面打开链接

​    _blank 在新的标签打开链接

内部跳转的超链接，通过修改href属性可以使超链接在页面内部进行跳转

  \#表示跳转到页面的顶部

  \#id 表示跳转到页面的指定位置

  id属性：在网页中可以为元素设置一个id属性，作为元素的唯一标识

#### 块元素和行内元素

在html中，元素可以被分为块元素和行内元素

  块元素（block）

  \- 块元素会独占页面的一行自上向下垂直排列

  \- 块元素用来对网页进行布局，将一个网页分成一块一块

  \- 最常用的块元素：div



  行内元素（inline）

  \- 行内元素只会占用自身的大小，自左向右水平排列

  \- 行内元素一般用来放置文字

  \- 最常用的行内元素：span



   替换元素

  \- img 图片替换

  \- iframe 网页替换

  元素的嵌套规则：

  \- 块元素中可以放置块元素，也可以放置行内元素

  \- 行内元素中尽量不放置块元素

  \- a元素中可以放置除它自身外任何元素

  \- p元素中不能放置块元素

####   内联框架

iframe

​    内联框架，用来向一个网页中引入另一个网页

​    属性：

​    src 来指定要引入的网页的路径

#### 图片标签

img

  \- 图片标签，用来向页面中引入图片

  \- 是自结束标签

  \- 属性

​     src：表示引入图片的路径

​     alt：对图片的描述，帮助搜索引擎来识别图片

​     如果不写alt，则搜索引擎不会对图片进行收录



  width

  \- 图片的宽度

  height

  \- 图片的高度

  -width和height两个属性只修改一个时，另一个会等比例缩放

  -实际开发中如果需要修改图片大小，建议只修改一个





  图片的格式：

  jpg：用来显示照片

​     支持的颜色丰富，不支持透明

  gif：用来显示颜色单一的图片或动图

​     支持的颜色少，支持简单透明

  png：用来显示颜色丰富的图片，支持透明效果

​    在网页中使用多

  webp：是谷歌专门为浏览器推出的一种格式

​     兼具上述格式所有优点，部分浏览器不支持这种格式

  base64：编码格式，编码后可以直接在网页中引入图片

​      通过base64对图片编码后，图片可以和网页一起加载，加快图片的加载速度

​      可以使用base64来加载一些对速度要求比较高的图片，但是不要大量使用



  选择图片的原则：

  图片大小一致，用显示效果好

  显示效果一致，选内存小的

  保证效果的同时，确保图片小

#### 相对路径和绝对路径

 路径有两种：

  1.相对路径

   \- 用来引入我们自己的项目内的图片

   \- 相对路径需要使用 ./开头或者../开头

   ./表示当前目录，比如当前的Day2, ./可以省略

   ../表示当前目录的上一级目录，比如CLIENT_HTML5_CSS3

   几个../就表示上几级

  2.绝对路径

  https开头

### Day2

#### css简介

CSS 

  \- 层叠样式表

  \- 通过CSS可以为网页中元素设置各种样式，让页面变得更漂亮



  1.内联样式（行内样式）

​    \- 可以直接将CSS编写在style属性中



​    一个网页分为三个部分

​     -结构、表现、行为

​     一个设计优良的网页，最好要把结构、表现、行为三者分离

​     目的是为了降低代码之间的耦合度,使代码更易维护



  2.内部样式表

​    \- 可以通过style标签来创建一个内部样式表

  3.外部样式表

​      -将样式写在外部的css文件中，然后通过link标签引入外部的样式

​      通过外部样式表，将结构和表现完全分离，使代码易于维护

​     同时代码可以在不同的页面之间进行复用

​     并且外部文件可以利用到浏览器的缓存机制，加快用户的访问速度

#### css基本语法

​    选择器 ：用来指定要设置样式的元素

​    声明块：用来设置样式

​        由一对大括号括起来

​        声明块里面是一个一个声明

​        声明是一个名值对：

​          一个样式名对应一个或多个样式值，之间使用冒号链接，分号结尾

#### 选择器

基本选择器

​      \- 元素选择器：根据标签名选择多个元素

​       语法：标签名{}

​       例如：p{}  div{}



​      \- id选择器：根据元素的id属性选中一个元素

​       语法：#id{}

​       例如：#p1{} #box{} 



​      \- 类选择器：与id类似，每一个元素都可以指定，用来为元素进行分类

​           和id不同，可以为多个元素指定相同的class，拥有同一个class的元素可以说™是一类

​          可以同时为一个元素指定多个class

​           语法：.class{}

​           例如：.p1{} .p2{} .p3{}

​      \- 通配选择器：选择页面中所有的元素

​         语法：*{}

 属性选择器

​     \- 用来根据元素的属性来选中元素

​     \- 语法：

​      [属性名] 选中具有该属性的元素

​      [属性名=属性值] 选中指定属性值的元素

​      [属性名^=属性值] 选中属性值以指定内容开头的元素 

​      [属性名$=属性值] 选中属性值以指定内容结束的元素

​      [属性名*=属性值] 选中属性值包含指定内容的元素



​    交集选择器：

​      \- 选中同时符合多个选择器元素

​      \- 语法：选择器1选择器2选择器3{}

​      例如：div[title=hello]

​        div.box{}

​        div#box1{} 不推荐使用，#box1就已经可以选中，如果使用这种说明css文件某些地方写错了



​     分组选择器：同时选中多个选择器对应的元素

​     语法：选择器1，选择器2，选择器3……选择器n{}



​    关系选择器：

​      \- 根据元素之间的关系来选中元素

​      \- 元素之间关系：父子、祖先后代、兄弟

​    子元素选择器：

​      作用：选中指定元素的子元素

​      语法：父元素>子元素{}

​    后代元素选择器：

​      作用：选中指定元素的后代元素

​      语法：祖先 后代{}

​    兄弟元素选择器：

​      作用：选中指定的兄弟元素

​      语法：兄+弟{}  选中紧随其后的一个兄弟

​         兄~弟{} 选中后边的所有兄弟元素

#### 伪类

伪类：https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes

伪类是一个特殊的类，用来表示元素的状态,伪类使用：开头

  像超链接，一个超链接有没有被访问过就是一种特殊的状态

  在css中，可以使用:visited来表示访问过的 超链接



  link、visited是链接用的

  hover、active是元素通用的 

 link和visited没有先后之分，hover必须写在active前面

  a的伪类：

​    :link

​      -表示正常的超链接（未访问过的）

​    :visited

​      \- 访问过的链接,根据用户的历史记录进行判断，由于隐私原因，通过visited只能改变文字的颜色

​    :hover

​      \- 鼠标移入的元素

​    :active

​      \- 鼠标点击

  

  结构伪类：

​    :root

​      \- 根元素，相当于html

​    :empty

​      \- 空元素,里边没东西的，空格也算有内容

​    :first-child

​      \- 第一个子元素

​    :first-of-type 

​      \- 同类型里的第一个子元素  

​    :nth-child

​      \- 第n个子元素,2n表示偶数，2n+1表示奇数，n+2表示从第二个元素开始

​	  - even 表示偶数，相当于2n

​        odd 表示奇数，相当于2n+1

​    :nth-of-type

​      \- 同类型中的第n个子元素

​    :nth-last-child

​      \- 倒数第n个元素

​    :nth-last-of-type

​      \- 同类型中倒数第n个元素   

​    :last-child

​      \- 最后一个子元素

​    :last-of-type

​      \- 同类型中的最后一个子元素

​    :only-child

​      \- 唯一的子元素

​    :only-of-type

​      \- 同类型中唯一的子元素

​     :not

​      \- 否定伪类，除了某些元素

#### 伪元素

​    \- 伪元素表示的是页面中特殊的位置

​    \- 伪元素使用::开头

​    ::before

​      \- 元素开始的位置

​    ::after

​      \- 元素结束的位置

​    ::first-letter

​      \-  首字母

​    ::first-line

​      \- 首行

​    ::selection

​      \- 选中的文字的样式



通过before、after可以选中元素开始或结束的位置，从而为其添加内容

​      注意：这里的内容是通过CSS添加的！！不算是网页中的正式内容

​      1.通过它可以为元素添加一些统一的符号

​      2.也可以在特殊场景下通过他们来调整一下页面的样式

### Day3

#### 选择器的权重

样式的冲突

​        \- 当我们使用不同的选择器选中同一个元素并设置相同的样式时，就发生了样式冲突

​        \- 当样式冲突发生时，哪个样式生效由选择器的优先级（权重）决定



​        -比较优先级时，需要将多个选择器的优先级一起计算

​          优先级高的优先显示，优先级的累加无法跨越数量级

​          例如：#box  还是#box大

​            .box1.box2.box3.box4.box5.box6{}

​          如果优先级一样，则优先显示靠下的样式

​          如果为样式添加!important，则该样式会获得最高的优先级（慎用），如果有两个important就看选择器



​          注意：分组选择器优先级都是单独计算的！！！

​          例如：div，#box1,.box2{}=div{}#box1{}.box2{}





​        继承的样式：没有优先级

​        通配选择器：0，0，0，0

​        元素选择器：0，0，0，1

​        类和伪类选择器：0，0，1，0

​        id选择器：0，1，0，0

​        内联样式：1，0，0，0

从下往上优先级依次变小

#### 样式的继承

​      \- 设置给祖先元素的样式，也会同时应用到其后代元素上

​      \- 继承的存在大大的简化了样式的编写



​      但并不是所有的样式都会发生继承！！！

​      所有的布局、背景、边框相关的样式都不会发生继承

####       长度单位

​        像素（px）

​          显示器的图形实际上是一个个小点点构成的

​          每一个小点就是一个像素

​          每一台设备的像素大小是不同的，越清晰的设备像素越小

​        百分比（%）

​        设置后元素的属性会根据父元素指定属性的百分比计算

​         em

​            1em=当前font-size的大小，默认的字体大小是16

​         rem

​             1rem=1根元素的font-size（html根元素）

#### 颜色单位

​        1.颜色名

​          -直接使用颜色名来设置颜色

​          比如red，green，blue，yellow……

​        2.RGB值

​          \- 通过三种不同的颜色的组合，来调配出不同的颜色

​          \- 语法：RGB（红色，绿色，蓝色）

​          \- 取值范围：0-255

​          \- 光的三原色 全0黑色，全255白色

​       3.rgba（红色，绿色，蓝色,不透明度）

​          不透明度需要一个0-1之间的值

​       4. hsl()

​          \- h 色相 0-360

​          \- s 饱和度 0%-100%

​          \- l 亮度 0%-100%

​        5.通过三个两位的十六进制数字来表示一个颜色

​          语法：#红绿蓝

​            -每一个颜色的取值范围 00-ff

​            例如：红色：#ff0000

​               绿色；#00ff00

​            如果rgb值是两两重复的，可以进行简写

​              \#aabbcc->#abc

​              \#bbffaa->#bfa

​              \#ff0000->#f00

### Day4

#### 边框 

border-width 用来指定边框的宽度

​           10px 20px 30px 40px 上 右 下 左

​           10px 20px 30px 40px 上 左右 下

​           10px 20px  上下 左右

​           5px 则四个边框都是5px



​           border-top-width   单独设置上面的边框

​           border-right-width  单独设置右边的边框

​           border-bottom-width  单独设置下面的边框

​           border-left-width   单独设置左边的边框



​           border-color 颜色1 颜色2 颜色3 颜色4 也是上右下左的顺序



​           border-style 

​              \- solid 实线

​              \- dotted 点状虚线

​              \- dashed 虚线

​              \- double 双线



​          border简写属性,可以同时设置边框的三个样式

​          border-xxx 简写属性

​          border-top

​          border-bottom

​          border-left

​          border-right

#### 可见框

盒子的可见框指可见的部分,大小由内容区.内边距,边框共同决定

​        box-sizing 用来指定盒子可见框的计算

​          \- 可选值

​            content-box 默认值,width和height用来设置内容区的大小

​            border-box 设置该值后,width和height用来设置盒子可见框的大小(会自动调整内容区大小)

#### 盒子模型

盒子模型（box model）

​      \- 网页的布局指的是将元素摆放到网页的不同位置

​      \- 布局就得先确定元素的大小

​      \- 在网页中每一个元素都是一个矩形，或者可以直接将其想象为是一个盒子

​       每一个盒子，都由以下几个部分组成：

​          \- 内容区（content）

​            \- 内容区在元素最内部，用来容纳子元素

​            \- 内容区的大小由width和height设置

​          \- 边框（border）

​            \- 边框是盒子边界，离开边框就属于盒子的外部了

​            \- 边框会影响到盒子可见框的大小

​          \- 外边距(margin)

​            -盒子与盒子之间的距离被称为外边距

​            \- 外边距不会影响盒子的大小,但是他会影响盒子的位置(实际大小)

#### 内边距

内容区和边框之间的距离称为内边距

​        共有四个方向的内边距

​          padding-top 上内边距

​          padding-bottom 下内边距

​          padding-right  右内边距

​          padding-left  左内边距



​          简写属性padding

​           默认情况下,背景颜色会延伸到内边距上,所以我们无法直观的看到内边距

​           内边距也会影响到盒子可见框的大小

​           一个元素的可见框的大小由内容区,内边距,边框共同决定

#### 外边距

外边距同样有四个方向,可以有负数

​        margin-top 上外边距,值越大元素越靠下

​        margin-bottom 

​        margin-left 左外边距,值越大元素越靠右

​        margin-right 

​        由于浏览器默认是按照自左向右,自上向下的顺序来排列元素的

​        所以当我们设置上和左外边距时,是改变元素自身的位置

​        但是设置下和右时,会改变其他元素的位置



​      外边距的折叠

​        \- 垂直方向的相邻外边距会发生外边距折叠的现象

​          兄弟元素间外边距会取较大值

​          父子元素间子元素外边距会传递给父元素,这样会导致布局出问题,需要避免该问题

​          方法1:不用外边距,用内边距

​          方法2:用外边距的话,让他们不再相邻



​        可以将margin的值设置为auto,设置auto后,浏览器会自动计算外边距

​        当我们将margin-left或margin-right中的一个设置为auto时,则浏览器会自动使其尽量的大

​        如果我们将margin-left和margin-right都设置为auto时,浏览器会使元素左右的外边距相同,也就是元素会在其父元素中水平居中

​        通过将一个块元素的左右外边距设置为auto,以使其在父元素中水平居中

​        默认情况下,垂直外边距设置auto时,浏览器会自动取0为外边距

#### 行内元素的盒子模型

内容区

​        -行内元素的大小被内容撑开

​          无法通过width和height来设置行内元素的宽高

​      内边距

​        \- padding 行内元素可以设置内边距，但是垂直方向的内边距不会影响布局（会盖住别的元素）

​      边框

​        \- border 行内元素可以设置边框，但是垂直方向的边框不会影响到页面的布局（不会挤到别的元素）

​      外边距

​        -margin 行内元素可以设置水平方向的外边距

#### display和visibility

display

​      \- 用来设置元素的类型

​      \- 可选值：

​        inline 将元素设置为行内元素

​        block 将元素设置为块元素

​        inline-block 行内块元素

​              \- 行内块兼具行内元素和块元素的特点

​              \- 不独占一行，又可以设置宽高

​            注意：行内块的特点和文本很像，所以布局时尽量少用

​        none 隐藏元素

 visibility

​          \- 用来设置一个元素的可见性

​          \- 可选值：

​            visible 默认值 元素可见

​            hidden 元素是隐藏的在页面中不可见，但是依然占据页面的位置 

#### overflow

当子元素大小超过父元素内容区时，子元素会从父元素中溢出（overflow）

​      在css中通过在父元素中设置overflow这个样式来处理溢出内容

​      overflow

​        -设置元素如何处理溢出内容

​        \- 可选值：

​        visible，默认值，溢出的内容直接在元素外边显示

​        hidden 隐藏溢出的内容

​        scroll 生成双方向滚动条，通过滚动条来查看完整内容

​        auto 根据需要生成滚动条

### Day5

#### 重置样式

为了开发更方便，编写css样式前，我们通常都需要对默认样式进行重置 

​      方式一：

​          *{

​            padding: 0;

​            margin: 0;

​          }

​      方式二：

​        \- 使用reset.css

​        \- https://meyerweb.com/eric/tools/css/reset/reset.css

​        \- 直接清除掉默认样式

引入： <link rel="stylesheet" href="./reset.css"> 

​      方式三：

​        \- 使用normalize.css

​        \- https://necolas.github.io/normalize.css/8.0.1/normalize.css

​        \- 没有直接清除所有样式，而是将默认样式统一

引入：   <link rel="stylesheet" href="./normalize.css">

#### 垂直对齐

在网页中，每个文字被显示时都会有一个文本框与之对应

​        当我们设置元素的font-size时，实际上就是设置文本框的大小

​        在文本框存在一个位置叫做基线（baseline）



​        文字的垂直对齐

​          默认每个文字和父元素在垂直方向都是沿着基线对齐的



​           vertical-align:设置元素垂直对齐方式

​            可选值

​              \- baseline 默认值 子元素和父元素的基线对齐

​              \- top 子元素文本框的顶部和父元素文本框的顶部对齐

​              \- bottom 子元素文本框的底部和父元素文本框的底部对齐

​              \- middle 将元素的中线和父元素基线高度+x高度一半的位置对齐

​            在开发中经常通过vertical-align来消除图片下边的空白

#### 文本样式

 text-align:文本的水平对齐方式

​          可选值：

​            \- left 默认值，左对齐

​            \- center：居中对齐

​            \- right：右对齐

​            \- justify 两端对齐



​        网页中图片、行内块都可以使用文本对齐方式



​        text-indent:首行缩进，可以设置负数，可以利用负值隐藏网页中的一些元素，font-size：0也可



​        text-decoration：文本修饰

​          可选值：

​            \- none 默认值 没有修饰

​            \- underline 下划线

​            \- overline 上划线

​            \- line-through 删除线 

​        text-transform: 

​          可选值：

​            \- lowercase 小写

​            \- uppercase 大写

​            \- capitalize 首字母大写

​            \- none  默认值 防止更改所有字符大小写

#### 单行省略

​	/*禁止文字自动换行*/

​      white-space: nowrap;

​      /*禁止文字溢出*/

​      overflow: hidden;

​      /*溢出的内容以省略号显示*/

​      text-overflow: ellipsis;

#### 行高

line-height 用来设置元素的行高

​         行就是用来放文字的

​         行高就是文字所在行的高度，每行都有行高

​         文字默认是在行高中垂直居中     

​         行间距 = 行高 - 字体大小

​         行高可以设置一个数字，那么行高将会是字体大小对应的倍数

#### 字体

font-size  字体大小

​      font-weight 字重

​        可选值

​          \- normal 默认值 正常的粗细

​          \- bold 加粗

​          \- lighter 细的

​      font-style 字体的样式

​        可选值：

​          \- normal 默认值 正常的

​          \- italic 斜体

​      font-family 字体族，使用什么字体

​        \- 字体的分类

​          \- serif 衬线字体

​          \- sans-serif 非衬线字体

​          \- monospace  等宽字体 中文不涉及等宽



​        当我们将字体设置为上述类型时，浏览器会自动选择相应的字体来显示



​      font简写属性，可以同时设置字体的相关属性

​        \- font:前边任意，后边两个必须是font-size/line-height font-family

#### font-face

font-face 通过它可以将远程字体提供给用户使用

​          \- 使用的时候要慎用

​            1.下载字体需要花费时间，如果字体文件太大，用户可能无法第一时间下载完成

​            2.使用字体可能会涉及版权问题，小心律师函

@font-face {

​      /*src服务器中字体的路径*/

​      font-family: "test";

​      /*字体的名称，自定义*/

​      src: url("./font.ttf");

### Day6

#### 图标字体

在网页中，我们经常能看到一些图标，可以使用图片来表示这些图标

​      但是图片有一些不足

​        1.不便于缩放

​        2.无法改变颜色

​      

​      在网页中文字可以任意缩放和改变颜色（文字是矢量图）



​      所以出现了图标字体（iconfont）

​        所谓的图标字体指的是将小图标制作成字体文件

​        可以使用一些第三方库

​        https://fontawesome.com

​        https://remixicon.cn/

​        https://www.iconfont.cn/



​      https://fontawesome.com使用步骤:

​        1.下载(start-download)

​        2.解压缩

​        3.复制css和webfonts到项目下，可以只留个all.css

​        4.在页面中引入all.css

​        5.用法：在页面中添加标签

body中<i class="fa-sharp fa-solid fa-house"></i>

引入<link rel="stylesheet" href="./css/all.css">

​      https://www.iconfont.cn/使用步骤：

​        1.注册登录

​        2.选择图标加入购物车,添加至项目中

​        3.进入项目，下载至本地

​        4.将样式表和字体文件添加到项目中

​        5.引入css

​        6.通过类使用  

```
<i class="iconfont icon-calendar"></i>
```

​        实体

```
  <i class="iconfont">&#xe62c;</i>
```

#### 轮廓、圆角、阴影

outline 轮廓线 

​        \- 和边框非常像，但outline不会影响到元素可见框的大小，起到修饰作用

示例：outline: 10px solid red;

.box1:hover{

​        outline: 10px dashed red;

​      }

border-radius 圆角

border-top-left-radius: 200px; /*左上*/

​      border-top-right-radius: 200px;/*右上*/

​      border-bottom-left-radius: 200px;/*左下*/

​      border-bottom-right-radius: 200px;/*右下*/

简写属性：

​     border-radius:10px 20px 30px 40px 左上、右上、右下、左下

box-shadow：为元素指定阴影

 box-shadow: 10px 10px 10px 10px rgb(36,36,36,.3);

​        \- x轴偏移量 y轴偏移量 模糊半径 扩散半径 阴影的颜色；

​        可以设置一个inset来表示内部阴影 

#### 文档流

文档流 （normal flow）正常布局流

​        \- 文档流是网页中的位置，我们所创建的元素默认都存在于文档流中

​        \- 文档流中的元素必须要遵循文档流的规则在页面中排列

​           块元素

​            \- 块元素在文档流中自上向下垂直排列

​            \- 块元素的默认宽度会将父元素撑满（默认值为auto）

​            \- 块元素的默认高度被内容撑开

​           行内元素

​            \- 行内元素在文档流中自左向右水平排列，如果一行不足以容纳所有元素

​              则会另起一行继续自左向右水平排列

​            \- 行内元素的默认宽度和高度都被内容撑开

#### 水平布局的等式

子元素会在父元素内容区中排列

​        在文档流中，块元素的水平排列必须要遵循如下一个等式：

​          包含块内容区的宽度 = 子元素可见框宽度 + 子元素的水平外边距

​                    margin-left＋可见框＋margin-right

​                    100 + 200 + 100 = 800 此时右外边距会自动调整为500

​                    500 + 100 +　100 = 800 此时右外边距会自动调整为-200

​                    100 + auto + 100 = 800 宽度为auto，此时auto为600

​                    auto + 200 + auto =800

​                    auto + auto + 200 = 800

​            \- 当属性值中没有auto，此时浏览器会自动调整右外边距已使等式强制满足

​            \- 当属性值为auto，则浏览器会自动调整该值以使等式满足

​            \- 当左右外边距为auto，而width有值，则左右外边距会设置相等的值以使等式满足

​            \- 当外边距和width同时设置为auto，则外边距的auto为0



​          在文档流中，块元素的垂直排列，不需要遵循等式

#### 包含块

包含块（containing block）

​      \- 在文档流中，包含块就是离当前元素最近的祖先块元素

备注： 根元素（<html>）所在的包含块是一个被称为初始包含块的矩形。它具有视口（对于连续媒体）或页面区域（对于分页媒体）的尺寸。

### Day7

#### 浮动

浮动（float）

​      \- 是一种传统的网页的布局方式

​      \- 通过浮动可以使得元素脱离文档流而横向排列

​      可选值

​        \- none 默认值 不浮动

​        \- left 左浮动

​        \- right 右浮动

​      浮动的特点

​        1.设置浮动后，元素会脱离文档流，其后的元素会自动上移

​        2.设置浮动后，元素会向其包含块的左侧或右侧移动

​        3.如果一行之内容纳不下所有的浮动元素，那么后边的元素会自动换到下一行

​        4.浮动元素不会超过他上边浮动的兄弟元素，最多平行

​        5.浮动元素不会盖住文字，文字会环绕在浮动元素的周围

​        这是浮动的历史原因，浮动设计的初衷就是为了环绕文字元素

​        高度和宽度被内容撑开

​        脱离文档流后 ，行内元素就变成了块元素

​        脱离文档流之后就不再需要区分行内和块元素

浮动后，之前的布局等式就失效了



​      元素脱离文档流的特点

​      块元素

​       之前

​        1.自上向下垂直排列

​        2.宽度默认为父元素的全部

​        3.高度被内容撑开

​       之后

​        1.块元素不再独占一行，自左向右水平排列

​        2.宽度和高度都被内容撑开



​      行内元素

​        设置浮动行内元素可以设置宽度和高度



​        总结：脱离文档流后，块元素不再独占一行，宽高被内容撑开，行内元素变成块元素（只是特点一样，不是真的变成块元素）

#### 高度塌陷

在文档流中的元素，可以将其他元素的高度撑开

​        当元素浮动，他会脱离文档流，脱离后无法撑开父元素的高度，就导致父元素高度塌陷

​        父元素高度塌陷后，其后的元素会自动上移，导致布局变得混乱



​        高度塌陷是使用浮动时必须要解决的问题！！！



​        解决方法：

​          1.直接将父元素的高度写死

​            \- 问题：无法根据子元素的高度变化

​          2.BFC（Block Formatting Context）块级格式化环境

​           网址：https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_display/Block_formatting_context

​           可以将BFC理解为一个隐藏的属性，当开启BFC后元素会具备如下的特征：

​            1.子元素的垂直外边距不会传递给父元素

​            2.元素不会被浮动元素所覆盖

​            3.元素可以包含浮动的子元素



​            如何开启BFC

​              \- 需要用其他的样式来间接开启BFC

​              例如:

​                \1. 浮动会开启元素的BFC（会有副作用，使得其他元素也浮动了）

​                \2. 将overflow设置为一个非visible的值

​                3.display: flow-root 最佳方式，但不支持IE浏览器

​                4.根元素自带BFC ，表示我们整个网页其实就是在一个BFC中 

#### clear清除浮动

clear  谁受到影响，就对他进行清除

​        \- 清除浮动元素对当前元素产生的影响

​        可选值

​          \- left 清除左侧浮动元素对当前元素产生的影响

​          \- right 清除右侧浮动元素对当前元素产生的影响 

​          \- both 清除最大一侧浮动元素对当前元素的影响

#### clearfix

/*既能解决外边距折叠也能解决高度塌陷*/

​    .clearfix::after,

​    .clearfix::before{

​      content: "";

​      display: table;

​      clear: both;

​    }

### Day8

#### 垂直水平居中

盒子模型的等式

​        margin-left + 可见框宽度 + margin-right = 包含块的内容区的宽度



​        当元素开启了绝对定位后，两个新的等式诞生了！

​        left偏移量 + margin-left + 可见框宽度 + margin-right + right = 包含块的内容区宽度

​        top偏移量 + margin-top + 可见框高度 + margin-bottom + bottom = 包含块的内容区高度

​        auto + auto + 200 + auto + auto = 800 两边都是auto会位置不变

​        0 + auto + 200 + auto + 0 = 800  左右偏移量都是0就水平居中

​        0 + auto + 200 + auto + 0 = 800  上下左右偏移量都是0垂直居中

#### 相对定位

定位（position）

​      \- 通过定位可以将元素摆放到页面中的任何位置

​      \- css中一共有4种定位

​        1.相对定位

​        2.绝对定位

​        3.固定定位

​        4.粘滞定位

position  用来设置元素的定位方式

​      可选值

​        \- static 默认值，元素没有开启定位

​        \- relative 相对定位

​        \- absolute 绝对定位

​        \- fixed 固定定位

​        \- sticky 粘滞定位

​      相对定位

​        \- 将元素的position属性设置成relative则开启了元素的相对定位

​        相对定位的特点

​          1.开启相对定位而不设置元素的偏移量，此时元素不会发生任何变化

​          2.开启相对定位不会使得元素脱离文档流，不会改变元素的性质

​          3.相对定位元素是参照于其原来的位置进行定位的

​          4.相对定位会提升元素的层级（会盖住文档流的元素）



​        偏移量

​          \- 开启了定位的元素可以通过偏移量来设置元素的位置

​          \- 偏移量通常只用设置两个即可定位一个元素的位置

​          偏移量有四个

​            \- top   元素上边距离定位位置上边的距离

​            \- bottom  元素下边距离定位位置下边的距离

​            \- left   元素左边距离定位位置左边的距离

​            \- right  元素右边距离定位位置右边的距离

#### 绝对定位

绝对定位

​        \- 将元素的position设置成absolute，则开启了元素的绝对定位

​        特点：

​          1.开启绝对定位后，如果不设置偏移量，元素的位置不会发生变化

​          2.开启绝对定位后，元素会脱离文档流，同时元素的性质发生变化(块元素不独占一行，宽高被内容撑开，行内元素变成块元素)

​          3.绝对定位是参照于他的包含块进行定位的

​            \- 绝对定位的包含块离他最近的开启了定位的祖先元素

​            \- 如果所有的祖先都没有开启定位，则它的包含块是初始包含块

​            \- 初始包含块的大小和视口相同

​          4.绝对定位会提升元素的层级（会盖住别的元素）

#### 固定定位

 固定定位 position：fixed

​        固定定位也是一种绝对定位，所以他的大部分特点和绝对定位相同

​          不同点在于固定定位总是参照于浏览器的窗口进行定位

​          一旦定位，不会随窗口进行滚动

#### 粘滞定位

粘滞定位 position: sticky

​          粘滞定位的特点和相对定位相似

​          粘滞定位的参照物是离他最近的拥有滚动条的祖先元素

#### z-index

开启了定位后，可以使用z-index来设置元素的层级

​        z-index的值越大，元素的层级就越高，层级越高越优先显示

​        如果层级一样，则优先显示下面的元素(body里在下面的元素)



​        注意：祖先元素的层级再高，也无法盖住后代元素

​        z-index可以设置负值，设置负值后定位元素将会被文档流中的元素覆盖

### Day9

#### 布局方法总结

传统的布局手段

​      1.盒子模型（box model）

​        \- 主要用来确定元素的大小和间距

​        \- 主要用来处理网页的纵向排列

​      2.浮动（float）

​        \- 本来是用来处理文字环绕图片效果，后来被用到了元素的水平排列中

​        \- 因为他不是被设计用来布局的，所以使用浮动时会存在一些问题（高度塌陷问题）

​        

​        注意：

​          盒子模型和浮动主要用来进行宏观的布局



​      3.定位（position）

​        \- 通过定位可以将元素摆放到网页的任意位置

​        \- 主要用来设置网页中一些小组件

#### 定位的总结

相对定位

​      \- 不脱离文档流

​      \- 参照元素在文档流中的位置进行定位

​    绝对定位

​      \- 脱离文档流

​      \- 参照元素的包含块进行定位

​      \- 在网页中定位的主要手段就是绝对定位，相对定位更多的是配合绝对定位

​    固定定位

​      \- 脱离文档流   

​    粘滞定位

​      \- 元素紧紧的黏在某个位置

​    偏移量（offset）

​      \- 四个偏移量，可以有四种组合方式

​      top left 左上

​      bottom left 左下

​      top right 右上

​      bottom right 右下

#### 弹性容器的样式



弹性盒是CSS3中新添加的布局方式，通过他可以更加方便的完成我们对网页的布局

​      通过弹性盒模型，可以便捷完成网页中的各种布局



​      弹性容器

​        \- 要使用弹性盒必须先将元素设置为弹性容器

​        display：flex 块级弹性容器

​        display：inline-flex 行内弹性容器

​      弹性子元素（弹性项）

​        \- 弹性容器的子元素都会自动变成弹性子元素

​        \- 弹性子元素都会沿着弹性容器的主轴排列

​      主轴

​        \- 主轴就是弹性子元素排列方向



​      如何设置主轴方向：flex-direction

​                可选值：row 自左向右水平排列

​                    column 自上向下垂直排列

​                    row-reverse 自右向左水平排列

​                    column-reverse 自下向上垂直排列

​      设置元素是否换行：flex-wrap

​                可选值：nowrap 不自动换行

​                    wrap 自动换行

​                    wrap-reverse 反向换行

​      flex-flow:

​        flex-direction和flex-wrap的简写属性，没有顺序和数量的要求



​      justify-content 设置元素在主轴上的对齐方式

​          可选值：start  默认值，元素靠主轴起始位置对齐

​              end 元素靠主轴的结束位置对齐

​              center 元素沿主轴方向居中对齐

​              space-between 将主轴方向空白位置分配到两个元素之间

​              space-around 将主轴方向空白位置分配到元素周围

​              space-evenly 将主轴方向空白位置分配到元素的一侧



​      

​      侧轴（辅轴）

​        -侧轴是与主轴垂直方向的轴



​      align-items 设置元素在侧轴上的对齐方式  

​          可选值：start 元素靠侧轴起始位置对齐

​              end 元素靠侧轴的结束位置对齐

​              center 元素在侧轴上居中对齐

​              stretch 拉伸，元素会自动拉伸将侧轴撑满

​      align-content 设置元素在侧轴上空白空间的分配

​              space-between 将侧轴方向空白位置分配到两个元素之间

​              space-around 将侧轴方向空白位置分配到元素周围

​              space-evenly 将侧轴方向空白位置分配到元素的一侧



​        元素居中的方式：

​          1.margin：0 auto 水平居中

​          2.定位实现水平和垂直居中

​          3.弹性盒实现水平和垂直居中

#### 弹性子元素样式

​        flex-basis 弹性子元素的基础大小,根据主轴的方向自动设置width和height

​              主轴水平，设置宽度

​              主轴垂直，设置高度

​          可选值：auto 默认值，依据元素的宽高为准

​        flex-shrink 弹性子元素的收缩系数

​           \- 当父元素容纳不下所有子元素时，如何自动缩小元素大小

​           \- 元素的收缩是根据flex-basis和flex-shrink综合计算的

​              收缩系数越大，元素基础大小越大，元素就缩的越多

​           \- 默认值为1，如果设置为0表示不收缩

​        flex-grow 弹性子元素的生长系数

​           \- 容器中的富余空间分配给子元素

​           \- 默认值为0，元素默认不会变大

​        flex 上述三个的简写属性

​          -属性顺序：grow shrink basis

​          可选值：initial，默认值，相当于0 1 auto

​              auto 相当于 1 1 auto

​              none 相当于 0 0 auto

​		 align-self

​        弹性子元素的样式，用来单独设置某个弹性子元素的对齐方式

   	    order：数字  用来指定弹性子元素的位置

### Day10

#### 雪碧图

当我们第一次使用按钮时，在按钮上会有闪烁的情况出现

​        这是因为浏览器在加载外部资源时，是以懒加载（用的时候加载，不用不加载）的形式来完成的

​        像hover，active这些图片都是在按钮状态触发时才加载的，网速即使再快也要时间来完成加载

​        在图片加载完成前，超链接处在没有背景图片可以显示的状态，所以才会显示空白



​        我们可以使用CSS-Sprite来解决这个问题

​          \- 所谓CSS-Sprite就是指将多个小的图片统一放入一个大图片（雪碧图）中

​            然后通过偏移量来切换到不同的图片        

​          \- 使用CSS-Sprite可以将多个小图片进行整合，减少客户端发送请求的次数，提升用户体验

​          \- 在早期的网页中，几乎所有的小图标都是通过雪碧图来实现的，随着图标字体的广泛使用，雪碧图的使用也相对变得少了一些

​            

​          雪碧图

​            1.雪碧图是位图，位图放大会失真

​            2.雪碧图无法修改颜色

​            3.雪碧图支持彩色图标

​          图标字体

​            1.图标字体是矢量图，放大不会失真

​            2.图标字体可以任意修改颜色

​            3.图标字体只支持单色图标

#### 背景样式

background-color 背景颜色

​        background-image 背景图片

​        background-repeat 背景的重复方式

​            可选值

​              \- repeat 默认值，背景图片会沿元素的水平和垂直双方向重复

​              \- repeat-x 水平方向重复

​              \- repeat-y 垂直方向重复

​              \- no-repeat 不重复

​              \- space 背景图片充满元素，无法完整充满的使用空格隔开

​              \- round 背景图片自动缩放以充满元素

​        background-position 设置背景图片的位置

​            可选值

​              \- top left right bottom center 

​              任选两个值设置，如果只写了一个值，第二个默认为center

​        background-position:水平偏移量 垂直偏移量

​          水平偏移量值越大，背景图片越右移，可以设置负值

​          垂直偏移量值越大，背景图片越下移，可以设置负值

background-clip 设置背景图片显示区域

​        可选值

​          \- border-box 默认值，背景会延伸到边框的下边

​          \- padding-box 背景会延伸到内边距下

​          \- content-box 背景只在内容区显示

​      background-origin 设置背景图片定位的原点

​        可选值

​          \- padding-box 默认值，背景相对于padding定位

​          \- border-box 背景相对于边框定位

​          \- content-box 背景相对于内容区定位

​      background-image:linear-gradient(度数，颜色1，颜色2……) 一个函数，线性渐变

​      background-image:radial-gradient(circle at center, red 0, blue, green 100%);

​      在容器中心的渐变，从红色开始，变成蓝色，最后变成绿色    径向渐变



/* 简写属性,没有数量和顺序要求*/

​      background: #bfa url("../Day2/1.gif") no-repeat top center fixed;

 	 background-attachment:fixed; 决定背景图像的位置是在视口内固定，或者随着包含它的区块滚动

background-size 设置背景图片的尺寸

​        background-size：200px auto 宽200高自动 

​        background-size：auto 200px 宽自动高200

​        background-size: 100% auto;

​        background-size: cover 设置contain可以缩放图片使得图片在元素中完整显示，元素可能会有空白

​        background-size: contain 设置cover可以缩放图片使得图片在元素中撑满，图片可能显示不全

​        简写属性时background-size在偏移量后边加个/写

#### 表格（table）

​      \- 和日常生活中的一样，在网页中也可以创建表格

​      \- 可以通过表格来表示一些格式化的数据



​      使用table来创建一个表格

如果在table中没有写tbody，则浏览器会自动创建tbody，并将所有的tr都放入tbody中

  colspan 横向合并单元格

  rowspan 纵向合并单元格

<table>

<!-- 表格头部 -->

​    <thead>

​		tr表示一行

​         td表示一个单元格

​         th表示表头中的单元格

​         caption 表格标题

</thead>

​    <!-- 表格主体 -->

​    <tbody>

</tbody>

​    <!-- 表格底部 -->

​    <tfoot>

</tfoot>

</table>

#### 表格对齐方式

td设置：

​	text-align: center;

​      /* 文字在td中会自动垂直居中 */

​      vertical-align: middle;

### Day11

#### 表单

表单（form）

​      \- 在网页中通过表单将信息提交给服务器 

​    使用form标签来创建一个表单

​    action用来指定表单要提交到哪里

​    文本框：input type=text，如果希望表单中的数据真的被提交给服务器，必须为表单指定name属性

​    提交按钮：input type=submit，可以通过value属性来修改按钮上的文字

​    密码：input type=password，默认情况下，表单中的数据会通过url地址发送，url地址后的？被称为查询字符串（query string）

​        ?hello=1&password=12，查询字符串是一个个名值对结构，一个数据名对应一个值，多个名值对之间使用&隔开，

​          数据发送给服务器后，服务器可以根据数据名获取对应的值

​    单选框：input type=radio，单选框是根据name属性来分组的，相同name属性为一组，像这种选择框，不需要用户填写内容，还必须为表单项指定value属性，value最终会成为提交给服务器的值

​    多选框：input type="checkbox" name="" value=""

​    下拉框：使用select，option来创建下拉列表，添加multiple属性后可以将下拉列表设置为多选的下拉框

​    重置按钮：input type="reset"

​    普通按钮：input type="buttom" 只能被点，但是我们可以通过js为其添加功能



​     <label for="username">用户名</label>

​      <input type="text" name="hello" placeholder="请输入用户名" value="admin" id="username"> label和input关联起来，点击用户名就能直接点到文本框

#### 表单属性

​	placeholder 用来设置文本框的占位符

​    value 文本框中可以通过value来指定默认值

​    disabled 禁用表单项，不会被提交

​    readonly 只读，表单项无法修改，但是可以提交

​    checked 默认选中的单选和多选

​    selected 默认选中的下拉项

#### 居中总结

1.利用盒子模型margin：0 auto来实现水平居中

​        \- 原理：利用盒子模型水平布局的等式

​          左右外边距+可见框宽度=包含块的宽度

​        \- 缺点：1.不能实现垂直居中

​            2.居中的元素必须指定宽度

​      2.利用定位

​        position: absolute;

​        top: 0;

​        bottom: 0;

​        right: 0;

​        left: 0;

​        margin: auto;

​      \- 原理：利用定位后新的等式来实现居中

​        左右偏移量+左右外边距+可见框宽度=包含块宽度

​        上下偏移量+上下外边距+可见框高度=包含块高度

​      \- 缺点：1.设置的样式多一些

​          2.居中的元素必须指定宽度

​      3.使用表格

​        父元素的设置

​          display: table-cell;

​          vertical-align: middle;

​        子元素的设置

​          margin：0 auto

​      或者

​        子元素的设置

​          display: inline-block

​        父元素的设置

​           text-align: center

​      \- 缺点：父元素设置为单元格后，默认宽度被内容撑开

​      4.利用弹性盒

​        父元素的设置

​          display: flex;

​          align-items: center;

​          justify-content: center;

​        \- 缺点几乎没有

### Day12

#### 隐藏元素

​	 1.不设置宽高 

​      2.display：none 不会占据位置

​      3.visibility：hidden 会占据位置

​      4.opacity：0 会占据位置

### Day13

#### 变形

通过变形可以对元素的位置、大小、角度等进行修改

​      transform用来设置变形

​        \- 需要通过不同的变形函数来实现元素的变形

​        \- 当我们对元素进行变形时，只会影响到元素自身，不会影响到其他元素的位置

​      translateX() x轴平移

​      translateY() y轴平移

​        设置平移时，如果使用百分百单位，百分百是相对于元素自身大小计算

#### 平移

​		transform: translateX(100px) translateY(100px) translateZ(500px);

​        transform: translate(100px,100px);

​        transform: translate3d(100px,100px,500px);

translateZ 用来设置Z轴平移

​          \- z轴平移视觉上会感到元素大小的变化

perspective 用来设置透视的效果

​          需要一个长度作为值，长度表示人眼与屏幕的距离

translateX  z轴平移

translateY y轴平移

#### 旋转

​	  transform: rotateX(10turn) rotateY(10turn) rotateZ(10turn);

​      transform: translateX(100px) rotateZ(45deg);

​      transform:  rotateZ(45deg) translateX(100px);

​      transform:  rotateZ(2turn) ;

​		rotateX 沿X轴旋转

​        rotateY 沿Y轴旋转

​        rotateZ 沿Z轴旋转

​          单位：

​            \- deg 度数

​            \- turn 圈

​        transform-origin 指定变形的原点

​        transform-origin: top center;  上边中间位置

#### 缩放

​		scaleX X轴缩放

​        scaleY y轴缩放

​        scaleZ z轴缩放

​        scale x y轴缩放

​		transform: scale(.2);

####  过渡

过渡（transition）

​        \- 通过过渡可以使得元素样式发生变化时，一点点的变化

​      transition-property 指定应用过渡属性的名称

​        \- all 表示所以样式

​      transition-duration 指定过渡动画所需的时间

​        单位：秒和毫秒 1秒=1000毫秒

​      transition-delay 在过渡效果开始作用之前需要等待的时间

​      transition-timing-function 指定过渡的时间的曲线（每一次过渡都会执行）

​          可选值

​            \- ease 默认值，先加速再减速

​            \- linear 匀速运动

​            \- ease-in 加速运动

​            \- ease-out 减速运动

​            \- 贝塞尔曲线 自定义运动方式

​            \- steps() 分步执行动画

​      transition 过渡的简写属性

​        \- 持续时间在前，延时在后，别的没要求

#### 3d立方体

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        body{
            perspective: 800px;
        }
        ul{
            list-style: none;
        }
        .cube{
            width: 200px;
            height: 200px;
            margin: 200px auto;
            position: relative;
            /* 开启3d效果 */
            transform-style:preserve-3d;
            transition: all 10s;

        }
        .cube:hover{
            transform: rotateX(1turn) rotateY(1turn);
            transform: rotateY(45deg) scale(2);
        }
        .cube li{
            width: 200px;
            height: 200px;
            opacity: .7;
            font-size: 50px;
            color: #fff;
            text-align: center;
            line-height: 200px;
            position: absolute;

        }
        .cube li:nth-child(1){
            background-color: tomato;
            transform: translateZ(100px);
        }
        .cube li:nth-child(2){
            background-color: rgb(255, 203, 71);
            transform: rotateY(90deg) translateZ(100px);
        }
        .cube li:nth-child(3){
            background-color: rgb(194, 255, 71);
            transform: rotateY(-90deg) translateZ(100px);
        }
        .cube li:nth-child(4){
            background-color: rgb(71, 255, 221);
            transform: rotateX(90deg) translateZ(100px);
        }
        .cube li:nth-child(5){
            background-color: rgb(99, 71, 255);
            transform: rotateX(-90deg) translateZ(100px);
        }
        .cube li:nth-child(6){
            background-color: rgb(255, 117, 71);
            transform: translateZ(-100px);
        }
    </style>
</head>
<body>
    <ul class="cube">
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>
    </ul>
</body>
</html>
```

#### 动画

通过@keyframes来定义关键帧

​        from 表示动画的开始位置

​        to 表示动画的结束位置

```
@keyframes move {
            from {
                margin-left: 0;
            }

            to {
                margin-left: 500px;
            }
        }
 move是动画名字，自定义的
```

​      animation-name 指定动画的名字

​      animation-duration 指定一次动画执行的时间

​      animation-iteration-count 指定动画执行的次数

​            \- infinite 无限执行

animation-direction  动画的方向

​            可选值

​              \- normal 默认值

​              \- reverse 反向执行

​              \- alternate 正向反向交替执行

​              \- alternate-reverse 先反向再正向

​      animation-fill-mode 动画的填充模式

​            可选值

​              \- none 默认值 延迟时元素保持不变，动画执行结束时恢复原状

​              \- forwards 延迟时元素保持不变，动画执行结束时保持to状态

​              \- backwards 延迟时元素变为from状态，动画执行结束恢复原状

​              \- both 延迟时元素变为from状态，动画执行结束保持to状态

​      animation-play-state 动画的播放状态

​            可选值

​              \- paused 暂停

​              \- running 运行

​      animation 简写属性，持续时间在前，延时在后，别的没要求

### Day14

#### 布局回顾

​	第一代 原始布局:表格布局

​        缺点：1.不易于维护 2.对SEO搜索引擎不友好

​    第二代 CSS 浮动

​      

​    第三代 flex布局

​      \- 善于单行单列

​      \- 多行多列布局时，需要使用不同的结构组合使用

​      \- 结构复杂，样式简单

​    第四代 网格布局（grid）

​      \- 网格布局的方式和table类似

​      \- 在网格布局，将网页分为了一行一行和一列一列

​        通过这些行和列的设置帮助我们完成布局

​      \- 网格布局比较适用于复杂的布局

​      \- 相较于弹性盒，无需设置多余的结构

​      \- 结构简单，样式复杂

#### 精灵动画



```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box1{
            height: 271px;
            width: 132px;
            background-image: url("images/bigtap-mitu-queue-big.png");
            /* transition: background-position .3s steps(3); */
            animation: walk 1s steps(4) infinite;
            /* 设置steps()时，from不算第一步 */
        }
        /* .box1:hover{
            background-position:-396px 0;
        } */
        @keyframes walk{
            from{
               background-position: 0;
            }
            
            to{
               background-position: -528px 0;
            }
        }
    </style>
</head>
<body>
    <div class="box1"></div>
</body>
</html>
```

#### 钟表

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        .clock {
            position: relative;
            width: 500px;
            height: 500px;
            margin: 100px auto;
            border-radius: 50%;
            background-image: url("images/bg3.jpg");
            background-size: cover;
        }

        .hour {
            position: absolute;
            height: 40%;
            width: 8px;
            background-color: rgb(0, 0, 0);
            left: 0;
            right: 0;
            bottom: 50%;
            margin: 0 auto;
            transform: rotateZ(180deg);
            transform-origin: bottom center;
            animation: clock-run 43200s linear infinite;
        }

        .min {
            position: absolute;
            height: 45%;
            width: 6px;
            background-color: rgb(1, 1, 1);
            left: 0;
            right: 0;
            bottom: 50%;
            margin: 0 auto;
            transform: rotateZ(90deg);
            transform-origin: bottom center;
            animation: clock-run 3600s linear infinite;
        }

        .second {
            position: absolute;
            height: 48%;
            width: 4px;
            background-color: red;
            left: 0;
            right: 0;
            margin: 0 auto;
            transform: rotateZ(45deg);
            transform-origin: bottom center;
            animation: clock-run 60s steps(60) infinite;
        }

        /* 设置关键帧 */
        @keyframes clock-run {
            from {
                transform: rotateZ(0deg);
            }

            to {
                transform: rotateZ(360deg);
            }
        }
    </style>
</head>

<body>
    <div class="clock">
        <div class="hour"></div>
        <div class="min"></div>
        <div class="second"></div>
    </div>
</body>

</html>
```



#### 网格

网格容器

​        \- 要使用网格布局必须先设置网格容器

​        \- 使用display: grid; 或display: inline-grid;

​        \- 默认情况下，我们开启的是一个单列的网格布局

​      grid-template-columns 设置网格布局的列数（写几个就代表有几行）

​      grid-template-rows  设置网格布局的行数

​      repeat(10,2fr 1fr) 重复的设置 2fr和1fr重复10次，就是20

​      justify-items

​          \- 设置网格中元素水平方向的对齐方式

​        align-items

​          \- 设置网格中元素垂直方向的对齐方式

​      网格项

​        \- 网格容器的子元素都会自动的变为网格项

​      grid-column-start 网格列的起始位置

​      grid-column-end  网格列的结束位置

​      grid-row-start:  网格行的起始位置

​      grid-row-end: 3  网格列的结束位置

grid-column-end: span 2;/*占两份*/ 

可以通过z-index来调整网格项的层级

​    grid-column: 1/-1; 

​    \- grid-column-start和grid-column-end

​    \- 同时设置列开始和列结束



​    grid-row: 2/4;

​    \- grid-row-start和grid-row-start

​    \- 同时设置行开始和行结束



​    grid-area: 2/1/4/2;

​    \- grid-row-start/grid-column-start/grid-row-end/grid-column-end

​    \- 行开始/列开始/行结束/列结束

​    

​    grid-column-gap 列间距

​    grid-row-gap   行间距

​    简写：grid-gap:行间距 列间距

### Day15

#### 网格布局

​		justify-items align-items 网格项在轨道中的对齐方式



​        justify-self align-self 单独设置某一个网格项在轨道中的对齐方式

​        justify-content align-content 设置网格项整体对齐方式

#### 网格线命名

```
.outer{
            display: grid;
            border: 3px solid orange;
            grid-gap: 10px;
            grid-template-columns: [a] 200px [b] 200px [c] 200px;
            grid-template-rows: [head-row-start]200px [head-row-end side-row-start]200px [side-row-end]200px;
        }
        /* 
            可以为网格线命名
        
        */
        .outer div{
            border: 3px solid red;
        }
        .box1{
            grid-column: a/c;
            grid-row:head-row-start/ side-row-end;
        }
```

#### 命名区域布局

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .outer{
            display: grid;
            border: 3px solid orange;
            grid-gap: 10px;
            grid-template-columns: 200px 200px 200px 200px ;
            grid-template-rows: 100px 200px 200px 100px;
            grid-template-areas:
                "top top top top"
                "side main main main"
                "side main main main"
                "bottom bottom bottom ."
            
            ;
        }
        /* 
            grid-template-areas 可以设置命名的区域如何在容器中排布
        */
        .outer div{
            border: 3px solid red;
        }
        .box1{
            /* grid-column:1/-1; */
            grid-area: top;
        }
        .box2{
            grid-area: side;
        }
        .box3{
            grid-area: main;
        }
        .box4{
            /* grid-column:1/-1; */
            grid-area: bottom;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="box1">头部</div>
        <div class="box2">侧边栏</div>
        <div class="box3">主要内容</div>
        <div class="box4">底部</div>
    </div>
</body>
</html>
```

#### 自动行列

grid-auto-flow 设置网格项排列方式

​        row,默认值 优先填充行，行满了会自动创建新行

​        column 优先填充列，列满了会自动换到下一列，列满了会自动创建新列

​        dense 紧凑填充，自动填充空白位置，容器有位置后边的元素会自动填充到空白位置

​      grid-auto-rows 指定自动行的大小

```
grid-auto-rows: 100px 200px;/*第一行100，第二行200，第三行100,……交替*/
```

#### minmax函数

minmax 一个函数

​        minmax(最小值,最大值)

​        用于设置行和列的大小

​        可选值：像素、auto、min-content、max-content

​        例如：minmax(100px,300px)表示网格项的宽度最小为100px，最大为300px

​      repeat(auto-fill, minmax(100px,auto)) 

​        auto-fill，表示自动计算列，尽可能多的生成列

​        auto-fit，自动计算列，尽可能少的生成列

​        minmax(100px,auto)表示网格项的宽度最小为100px，最大为自动

​        也可以使用minmax(100px,1fr)表示网格项的宽度最小为100px，最大为1fr（占满剩余空间）

#### 移动端

像素（px）

​      \- 像素是屏幕上一个一个会发光的小点



​    分为物理像素和css像素

​      \- 物理像素：会发光的小点

​      \- css像素：编写样式时使用px

​    \- 我们编写样式时使用css像素，屏幕呈现图像时使用的是物理像素

​      默认情况下在pc中，一个css像素等于一个物理像素（1:1）

​    \- 当我们在浏览器中或系统中对网页进行缩放时，像素比会发生变化

​      比如，当我们将网页放大1.5倍时，css像素是不变的，而物理像素会变为原来的1.5倍大（1:1.5）



​    视口（viewport）：浏览器的可视区域被称为视口



​    移动端

​      \- 移动端的项目通常都会运行在手机中，

​        手机屏幕清晰度都是非常高的（物理像素越小，清晰度就越高）

​      \- 例如

​        显示器 

​          宽 两岔半 像素1920

​        手机   

​          宽 半岔 像素1170

​          

​      结论：手机的单个像素要远远小于显示器  

​      

​      如果直接将pc端的页面适配到手机上，效果是非常差的

​        \- 文字会非常小，无法阅读

​        \- 图片会非常小，无法查看

​        \- 布局会错乱，无法点击

​      为了使得pc端的页面在手机上正常显示，

​        在显示pc端时，移动端的浏览器会自动将视口宽度跳转为980px

​        如果pc端页面大小超过了980px，浏览器会自动对页面进行缩小，使得网页可以在浏览器中完整呈现

​        但是即使这样，网页在移动端浏览器的显示效果依然不佳



​      移动端浏览器，默认的像素比是980：xxxx

​      \- 每一个移动设备在出厂时，都会设计一个最佳的像素比，只有达到最佳像素比时，才能确保网页在移动端浏览器中显示效果最佳

​      \- 例如

​        iphone12

​          物理像素：1170px

​          最佳像素比：390px

​          像素比：1170/390 = 3

​      可以通过调整视口的大小来改变像素比



             <meta name="viewport" content="width=390px">iphone12的完美视口

​      当一个视口的宽度可以使得像素比变为最佳像素比时，这个视口（宽）就被称为完美视口



            <meta name="viewport" content="width=device-width">可以确保网页在任何设备下都有一个完美视口



​      适配问题

​        -开启完美视口后，任何移动设备都能获得一个最佳的浏览效果

​        但是这样却导致了不同设备下视口宽度不同

​        同样是390px，在12pro下时是全屏，se下就出现了滚动条，到ipad下就剩一半了

​        所以，我们就不能在移动端项目中使用px作为单位了

​        \- 解决方案

​          使用vw作为单位，vw=viewport width 视口宽度

​          1vw = 1%视口宽度



​        实际开发中，设计图的宽度都是像素为单位的，有375px、750px、1125px等

​        在将设计图转换为页面时，单位为vw

​        以750px宽的设计图为例 750px=100vw 1px=0.13333vw

​        所以在css中可以使用rem作为单位

### Day16

#### 媒体查询

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            color: red;
        }

        /* 
            @media 设备类型{}
                screen 带有屏幕的设备
                speech 屏幕阅读器
                print 打印设备
                all 任意类型设备
                min-width 指定最小视口，大于等于指定值时，样式生效
                max-width 指定最大视口，小于等于指定值时，样式生效
                , 或
                and 与
                not 非
                only 只，主要是避免一些兼容性的问题
        */
        /* @media (min-width:500px) and (max-width:800px) {
            body{
                background-color: orange;
            }
            
        } */
        @media only screen {
            body {
                background-color: orange;
            }
        }
    </style>
</head>

<body>
    <div>哈哈哈哈哈哈</div>
    <!-- 
        媒体查询（media query）
            - 通过媒体查询可以为不同的设备，不同的屏幕大小设置不同的样式
    -->
</body>

</html>
```

#### 移动端页面

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./css/all.css">
    <link rel="stylesheet" href="./css/index.css">
</head>

<body>
     <!-- 底部菜单 -->
      <nav class="menu">
        <ul>
            <li>
                <a href="#" class="active">
                    <i class="fa-solid fa-home"></i>
                </a>
            </li>
            <li>
                <a href="#">
                    <i class="fa-solid fa-user-circle"></i>
                </a>
            </li>
            <li>
                <a href="#">
                    <i class="fa-solid fa-heart"></i>
                </a>
            </li>
            <li class="shopping-cart">
                <a href="#">
                    <i class="fa-solid fa-shopping-bag"></i>
                </a>
            </li>
        </ul>
      </nav>
      <!-- 顶部搜索框 -->
    <form class="search-from" action="#">
        <input type="text" placeholder="Search keywords…">
        <i class="fa-solid fa-search"></i>
        <i class="fa-solid fa-sliders"></i>
    </form>
    <!-- 轮播图 -->
    <div class="page-hero">
        <ul class="img-list">
            <li>
                <a href="#">
                    <img src="./images/1.png" alt="">
                    <h2>20% off on your first purchase</h2>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="./images/1.png" alt="">
                    <h2>20% off on your first purchase</h2>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="./images/1.png" alt="">
                    <h2>20% off on your first purchase</h2>
                </a>
            </li>
            <li>
                <a href="#">
                    <img src="./images/1.png" alt="">
                    <h2>20% off on your first purchase</h2>
                </a>
            </li>

        </ul>
        <!-- 导航小点 -->
        <ul class="point">
            <a class="active" href="javascript:"></a>
            <a href="javascript:"></a>
            <a href="javascript:"></a>
            <a href="javascript:"></a>
    </div>
    <!-- 分类列表 -->
    <div class="cate-list">
        <header>
            <h3>Categories</h3>
            <a href="#">
                <i class="fa-solid fa-angle-right"></i>
            </a>
        </header>
        <ul class="cate-inner">
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-carrot"></i>
                    </span>
                    <span>蔬菜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>
            <li>
                <a href="#">
                    <span>
                        <i class="fa-solid fa-fish"></i>
                    </span>
                    <span>海鲜</span>
                </a>
            </li>

        </ul>
    </div>
    <!-- 特色商品 -->
     <div class="featured-products">
        <header>
            <h3>Featured-products</h3>
            <a href="#">
                <i class="fa-solid fa-angle-right"></i>
            </a>
        </header>
        <!-- 商品列表 -->
         <ul class="products">
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-regular fa-heart"></i>
                </div>
                <div class="add-cart">
                    <i class="fa-solid fa-shopping-bag"></i>
                    <span>Add to cart</span>
                </div>
            </li>
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-solid fa-heart"></i>
                </div>
                <div class="add-product">
                    <i class="fa-solid fa-subtract"></i>
                    <span class="count">1</span>
                    <i class="fa-solid fa-plus"></i>
                </div>
            </li>
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-regular fa-heart"></i>
                </div>
                <div class="add-cart">
                    <i class="fa-solid fa-shopping-bag"></i>
                    <span>Add to cart</span>
                </div>
            </li>
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-solid fa-heart"></i>
                </div>
                <div class="add-product">
                    <i class="fa-solid fa-subtract"></i>
                    <span class="count">1</span>
                    <i class="fa-solid fa-plus"></i>
                </div>
            </li>
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-regular fa-heart"></i>
                </div>
                <div class="add-cart">
                    <i class="fa-solid fa-shopping-bag"></i>
                    <span>Add to cart</span>
                </div>
            </li>
            <li>
                <div class="product-info">
                    <a href="#">
                        <div class="products-bg"></div>
                        <img src="./images/peach.png" alt="">
                        <span class="price">￥8.00</span>
                        <span class="title">Fresh Peach</span>
                        <span class="unit">dozen</span>

                    </a>
                    <i class="fa-solid fa-heart"></i>
                </div>
                <div class="add-product">
                    <i class="fa-solid fa-subtract"></i>
                    <span class="count">1</span>
                    <i class="fa-solid fa-plus"></i>
                </div>
            </li>
         </ul>
     </div>
    
</body>

</html>
```

#### 响应式布局

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./css/all.css">
</head>
<style>
    * {
        margin: 0;
        padding: 0;
    }

    .top-bar {
        position: relative;
        display: flex;
        height: 60px;
        background-color: black;
        color: #fff;
        align-items: center;
        padding: 0 20px;
    }

    .top-bar h1 {
        height: 34px;
    }

    img {
        width: 34px;
        height: 34px;
    }

    .top-bar .space {
        flex: auto;
    }

    .top-bar .user-info {
        margin-right: 40px;
    }

    .user-info .login {
        display: none;
        justify-content: center;
        align-items: center;
        position: absolute;
        height: 60px;
        width: 100%;
        left: 0;
        top: 60px;
        background-color: #000;
    }

    .user-info:active .login {
        display: flex;
    }

    .user-info .login::before {
        content: "";
        position: absolute;
        top: 0;
        width: 95%;
        height: 1px;
        background-color: #333;
    }


    .login a {
        flex: auto;
        text-align: center;
        text-decoration: none;
        color: #fff;
    }

    .menu .menu-inner {
        list-style: none;
        display: none;
        position: absolute;
        top: 60px;
        left: 0;
        width: 100%;
        background-color: #000;
    }

    .menu .menu-inner::before {
        content: "";
        position: absolute;
        left: 0;
        right: 0;
        margin: 0 auto;
        width: 95%;
        height: 1px;
        background-color: #333;
    }

    .menu:active .menu-inner {
        display: block;
    }

    .menu .menu-inner a {
        display: flex;
        background-color: rgb(0, 0, 0);
        padding: 20px 0;
        align-items: center;
        justify-content: space-between;
        font-size: 24px;
        text-decoration: none;
        color: #fff;
        margin: 0 40px;
    }

    @media (min-width:880px) {

        .menu i,
        .user-info i {
            display: none;
        }

        .top-bar .user-info .login {
            display: flex;
        }
        .user-info .login::before,
        .menu .menu-inner::before {
        display: none ;/* 在桌面视图下隐藏分隔线 */
    }

        .user-info .login {
            justify-content: center;
            align-items: center;
            position: static;
            height: auto;
            width: auto;
            font-size: 14px;
            font-weight: bold;
        }

        .user-info .login a:hover {
            color: #ff6700;
        }

        .top-bar .space {
            display: none;
        }

        .top-bar {
            justify-content: space-around;
        }

        .top-bar .menu {
            order: 2;
        }

        .top-bar .user-info {
            order: 3;
        }

        .top-bar .menu .menu-inner {
            display: flex;
            position: static;
            width: auto;
            background-color: #000;
        }

        .top-bar .menu .menu-inner a {
            display: block;
            font-weight: bold;
            padding: 0;
            font-size: 14px;
            margin: 0;
        }

        .menu .menu-inner a:hover {
            color: #ff6700;

        }

        .top-bar .menu .menu-inner a,
        .top-bar .user-info .login a {
            margin: 0 10px;
        }
    }
</style>

<body>
    <!-- 
        响应式布局
            - 网页会根据窗口大小的改变而改变
            - 响应式布局可以使得一个页面同时在多种设备中使用，降低我们开发的成本
            - 但是这种响应式页面，适合内容比较简单的页面
                如果是内容多的，布局复杂的页面还是建议pc端一套，移动端一套
            - 响应式布局主要就是借助媒体查询来实现的
            编写的原则：
                1.移动端优先
                2.渐进增强
                    - 确认断点
    
    -->
    <header class="top-bar">
        <h1>
            <a href="">
                <img src="../Mi/images/logo-mi2.png" alt="">
            </a>
        </h1>
        <div class="space">

        </div>
        <div class="user-info">
            <i class="fa-solid fa-user-circle"></i>
            <!-- 创建一个隐藏层 -->
            <div class="login">
                <a href="#">登录</a>
                <span class="line">|</span>
                <a href="#">注册</a>
            </div>
        </div>
        <div class="menu">
            <i class="fa-solid fa-bars"></i>
            <ul class="menu-inner">
                <li>
                    <a href="#">
                        <span>小米官网</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>小米影像</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>MIUI</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>loT</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>云服务</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>天星数科</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>有品</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>小爱开放平台</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>企业团购</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span>Location</span>
                        <i class="fa-solid fa-angle-right"></i>
                    </a>
                </li>
            </ul>
        </div>

    </header>
</body>

</html>
```

