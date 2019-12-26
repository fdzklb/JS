transform(变形)

transform可以用来设置元素的形状改变，主要有以下几种变形：rotate（旋转）、scale（缩放）、skew（扭曲）、translate（移动）和matrix（矩阵变形），语法如下：
.transform-class {
    transform ： none | <transform-function> [ <transform-function> ]*
}
transform-origin 基点
所有的变形都是基于基点，基点默认为元素的中心点。用法：transform-origin: (x, y)，其中 x 和 y 的值可以是百分比、rem 或者是 px 等等，也可以用表示位置的单词来表示例如：x 可以用left、center、right；y 可以用top、center、bottom。

scale 缩放
它有三种用法：scale(<number>[, <number>])、scaleX(<number>)和scaleY(<number>)；分别代表水平和垂直方向同时缩放、水平方向的缩放以及垂直方向的缩放，入参代表水平或者垂直方向的缩放比例。缩放比例如果大于1则放大，反之则缩小，如果等于1代表原始大小。

translate 移动
移动也分三种情况：translate(<translation-value>[, <translation-value>])、translateX(<translation-value>)和translateY(<translation-value>)；分别代表水平和垂直的移动、水平方向的移动以及垂直方向同时移动，移动单位是 CSS 中的长度单位：px、rem等;

skew 扭曲(拉伸)
扭曲同样也有三种情况，skew(<angle>[, <angle>])、skewX(<angle>)和skewY(<angle>)；同样也是水平和垂直方向同时扭曲、水平方向的扭曲以及垂直方向的扭曲，单位为角度




transition

transition是用来设置样式的属性值是如何从从一种状态变平滑过渡到另外一种状态，它有四个属性：

transition-property（变换的属性，即那种形式的变换：大小、位置、扭曲等）；
transition-duration（变换延续的时间）；
transition-timing-function（变换的速率）
transition-delay（变换的延时）
.transition-class {
    transition ： [<'transition-property'> || <'transition-duration'> || <'transition-timing-function'> || <'transition-delay'> [, [<'transition-property'> || <'transition-duration'> || <'transition-timing-function'> || <'transition-delay'>]]*;
}

transition-timing-function
它是来设置过渡效果的速率，它有6种形式的速率：
ease：逐渐变慢（默认），等同于贝塞尔曲线(0.25, 0.1, 0.25, 1.0)；
linear：匀速，等同于贝塞尔曲线(0.0, 0.0, 1.0, 1.0)；
ease-in：加速，等同于贝塞尔曲线(0.42, 0, 1.0, 1.0)；
ease-out：减速，等同于贝塞尔曲线(0, 0, 0.58, 1.0)；
ease-in-out：先加速后减速，等同于贝塞尔曲线(0.42, 0, 0.58, 1.0)；
cubic-bezier：自定义贝塞尔曲线。




animation

animation比较类似于 flash 中的逐帧动画，逐帧动画就像电影的播放一样，表现非常细腻并且有非常大的灵活性。
animation-name
它是用来设置动画的名称，可以同时赋值多个动画名称，用,隔开：

.animation {
    animation-name: none | IDENT[,none | IDENT]*;
}
animation-duration
它是用来设置动画的持续时间，单位为s，默认值为0：

.animation {
    animation-duration: <time>[,<time>]*;
}
animation-timing-function
和transition-timing-function类似：

.animation {
    animation-timing-function:ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(<number>, <number>, <number>, <number>) [, ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(<number>, <number>, <number>, <number>)]*;
}
animation-delay
它是来设置动画的开始时间，单位是s或者ms，默认值为0：

.animation {
    animation-delay: <time>[,<time>]*;
}
animation-iteration-count
它是来设置动画循环的次数，默认为1，infinite为无限次数的循环：

.animation {
    animation-iteration-count:infinite | <number> [, infinite | <number>]*;
}
animation-direction
它是来设置动画播放的方向，默认值为normal表示向前播放，alternate代表动画播放在第偶数次向前播放，第奇数次向反方向播放：

.animation {
    animation-direction: normal | alternate [, normal | alternate]*;
}
animation-play-state
它主要是来控制动画的播放状态：running代表播放，而paused代表停止播放，running为默认值：

.animation {
    animation-play-state:running | paused [, running | paused]*;
}
animation
它是animation-name、animation-duration、animation-timing-function、animation-delay、animation-iteration-count、animation-direction的简写：

.animation {
    animation:[<animation-name> || <animation-duration> || <animation-timing-function> || <animation-delay> || <animation-iteration-count> || <animation-direction>] [, [<animation-name> || <animation-duration> || <animation-timing-function> || <animation-delay> || <animation-iteration-count> || <animation-direction>] ]*;
}