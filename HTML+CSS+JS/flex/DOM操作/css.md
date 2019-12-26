div.setAttribute(
  'style',
  'background-color:red;' + 'border:1px solid black;'
);
上面的代码相当于下面的 HTML 代码。
<div style="background-color:red; border:1px solid black;" />

var divStyle = document.querySelector('div').style;
divStyle.backgroundColor = 'red';
divStyle.border = '1px solid black';

// HTML 代码为
// <div id="myDiv" style="color: red; background-color: white;"/>
var style = document.getElementById('myDiv').style;
style.item(0) // "color"
style.item(1) // "background-color"

CSSStyleDeclaration.removeProperty()
var style = document.getElementById('myDiv').style;
style.setProperty('border', '1px solid blue');