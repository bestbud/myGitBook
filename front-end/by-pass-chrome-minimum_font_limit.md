# 如何使Chrome显示小于12px字体？

Chrome会强制限制 `font-size` 设置小于`12px`文字显示为12px。

可以通过`transform: scale()`解决。下面以实现显示 8px 号字体为例，具体说明一下怎么做。
 
 - 将font-size设置为一个大于12px的值，通常我会设置目标大小的两倍, 方便计算scale。
 
   `font-size: 16px;`
 - 缩小
 
   `transform: scale(0.5);`
 - 位置调整： 默认是以中心为原点缩放的，缩放后字体对齐可能会被打乱，可以[设置原点](https://developer.mozilla.org/zh-CN/docs/Web/CSS/transform-origin)
 
   设置为以左侧中间为原点
   `transform-origin: 0 center`
    
   

