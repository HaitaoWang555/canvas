# canvas
## 绘制矩形
  1. 绘制一个填充的矩形`fillRect(x, y, width, height)`
  2. 绘制一个矩形的边框`strokeRect(x, y, width, height)`
  3. 清除指定矩形区域，让清除部分完全透明`clearRect(x, y, width, height)`
## 绘制路径
  1. 新建一条路径，生成之后，图形绘制命令被指向到路径上生成路径`beginPath()`
  2. 将笔触移动到指定的坐标x以及y上`moveTo(x, y)`
  3. 绘制一条从当前位置到指定x以及y位置的直线`lineTo(x, y)`
  4. 闭合路径之后图形绘制命令又重新指向到上下文中`closePath()`(不是必须的)
  5. 通过线条来绘制图形轮廓`stroke()`
  6. 通过填充路径的内容区域生成实心的图形`fill()`
  ```
  ctx.beginPath();
  ctx.moveTo(75, 50);
  ctx.lineTo(100, 75);
  ctx.lineTo(100, 25);
  ctx.fill();
  ```
## 绘制圆弧
画一个以（x,y）为圆心的以radius为半径的圆弧（圆），从startAngle开始到endAngle结束，按照anticlockwise给定的方向（默认为顺时针）来生成
`arc(x, y, radius, startAngle, endAngle, anticlockwise)`
`ctx.arc(75, 175, 50, 0, Math.PI * 2, true);`
## 二次贝塞尔曲线及三次贝塞尔曲线
  1. 绘制二次贝塞尔曲线，cp1x,cp1y为一个控制点，x,y为结束点 `quadraticCurveTo(cp1x, cp1y, x, y)`
  2. 绘制三次贝塞尔曲线，cp1x,cp1y为控制点一，cp2x,cp2y为控制点二，x,y为结束点 `bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)`
