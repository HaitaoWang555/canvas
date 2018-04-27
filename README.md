# canvas
## [绘制形状](shape.html)
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
## [颜色和样式](color.html)
  1. 设置图形的填充颜色`fillStyle = color`
  2. 设置图形轮廓的颜色`strokeStyle = color`
  3. 设置线条宽度 `lineWidth = value`
  4. 设置线条末端样式 `lineCap = type`
  5. 连接处样式  `lineJoin = type`
  6. 用 `setLineDash` 方法和 `lineDashOffset` 属性来制定虚线样式. `setLineDash` 方法接受一个数组，来指定线段与间隙的交替；`lineDashOffset` 属性设置起始偏移量
  7. 渐变 Gradients
      1. `createLinearGradient(x1, y1, x2, y2)` 渐变的起点与终点
      2. `createRadialGradient(x1, y1, r1, x2, y2, r2)` 前三个定义一个以 (x1,y1) 为原点，半径为 r1 的圆，后三个参数则定义另一个以 (x2,y2) 为原点，半径为 r2 的圆
      3. `gradient.addColorStop(position, color)` position 参数必须是一个 0.0 与 1.0 之间的数值，表示渐变中颜色所在的相对位置。
      4. 创建图形
  8. 图案样式 Patterns 
  9. 阴影
## [绘制文本](text.html)
  1. 在指定的(x,y)位置填充指定的文本，绘制的最大宽度是可选的`fillText(text, x, y [, maxWidth])`
  2. 在指定的(x,y)位置绘制文本边框，绘制的最大宽度是可选的`strokeText(text, x, y [, maxWidth])`
  3. 有样式的文本`font = value` `textAlign = value` `textBaseline = value` `direction = value`
  4. 预测量文本宽度 `measureText()`