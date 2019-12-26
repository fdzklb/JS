属性
document.defaultView//返回window对象
document.doctype
document.documentElement//返回root节点
document.body/head
document.scrollingElement//返回滚动元素
*document.activeElement//返回获得当前焦点的dom元素
document.fullscreeElemnt

节点属性集合
d.links
d.forms
d.images
...

文档静态信息属性
d.documentURL
d.URL
d.domain
d.location
d.lastModified
d.title
...
文档状态属性
...

方法
d.open()/close()/write()/writeln()
*d.querySelector(css选择器)/querySelectorAll(选择器)
*d.getElementsByTagName()[index]
*d.getElementsByClassName()[index]
*d.getElementsByName()//form radio img frame 
*d.getElementsById()
*d.createElement('<div>')
d.createTextNode()
d.createAttribute()
node.setAttribute()

d.createEvent(EventType)//uiEvent MouseEvent MutationEvent HtmlEvent
// 添加事件监听函数
document.addEventListener('click', listener, false);
// 移除事件监听函数
document.removeEventListener('click', listener, false);
// 触发事件
var event = new Event('click');
document.dispatchEvent(event);

var btn = document.getElementById('btn');
var mydiv = document.getElementById('mydiv');
btn.addEventListener('click', function () {
  mydiv.hidden = !mydiv.hidden;
}, false);


var focused = document.hasFocus();
var node = document.adoptNode(externalNode);
document.appendChild(node);

var node = document.importNode(externalNode, deep);
