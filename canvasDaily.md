## CANVAS

### 创建 context 对象
* var cxt=c.getContext("2d");
* getContext("2d") 对象是内建的 HTML5 对象，拥有多种绘制路径、矩形、圆形、字符以及添加图像的方法。

### 绘图

```js
    cxt.fillStyle = '#d1d1d1';	//颜色填充
	cxt.fillRect(x,y,width,height)	//绘图
```

### 绘线
* stroke() 方法会实际地绘制出通过 moveTo() 和 lineTo() 方法定义的路径。默认颜色是黑色

```js
    var c=document.getElementById("myCanvas");
    var ctx=c.getContext("2d");
    ctx.beginPath();
    ctx.moveTo(20,20);
    ctx.lineTo(20,100);
    ctx.lineTo(70,100);
    ctx.strokeStyle="green";	//颜色
    ctx.stroke();
```

### 绘圆
* context.arc(圆心的x坐标,圆心的y坐标,圆的半径r,起始角,结束角,方向);
* 如需通过 arc() 来创建圆，请把起始角设置为 0，结束角设置为 2*Math.PI。

```js
// 实心圆

var c=document.getElementById("myCanvas");
var cxt=c.getContext("2d");
cxt.fillStyle="#FF0000";
cxt.beginPath();
cxt.arc(70,18,15,0,Math.PI*2,true);
cxt.closePath();
cxt.fill();

//空心圆

var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.beginPath();
ctx.arc(100,75,50,0,2*Math.PI);
ctx.stroke();

```