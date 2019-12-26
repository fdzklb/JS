1.  flex-direction
决定主轴的方向：row|row-reverse|column(主轴为垂直方向，起点在上)|column-reverse

2.  flex-wrap
flex-wrap:nowarp|warp|warp-reverse(换行方式)

3.  flex-flow



4.  justify-content(对齐方式)
flex-start|flex-end|center|space-between|space-around

5.  align-items(在交叉轴如何对齐)
flex-start|flex-end|center|baseline(项目第一行文字的基线对齐)|stretch

6.  align-content(多条轴线的对齐方式)
box {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}


项目属性
7.  order
order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。

8. flex-grow
flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。

9. flex-grow属性
flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。
.item {
  flex-grow: <number>; /* default 0 */
}
如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。
如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。

10. flex-shrink属性
flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。
如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。

11. flex-basis属性
flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。
浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
.item {
  flex-basis: <length> | auto; /* default auto */
}
它可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。

12. flex
flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。

13. align-self属性
align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。
默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}