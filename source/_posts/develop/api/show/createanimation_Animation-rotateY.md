---
title: Animation.rotateY
header: develop
nav: api
sidebar:  createanimation_Animation-rotateY
---
 
 
**解释**：从 Y 轴顺时针旋转一个角度

**方法参数**：Number deg

**参数说明**：deg的范围-180~180，在Y轴旋转一个 deg 角度。

**代码示例**

<a href="swanide://fragment/029b22bb84ed13c34666162d600f82071574215498426" title="在开发者工具中预览效果" target="_self">在开发者工具中预览效果</a>

* 在 swan 文件中

```html
<view class="wrap">
    <view class="animation-element-wrapper">
        <view class="animation-element" animation="{{animation}}"></view>
    </view>
    <view class="card-area">
        <view class="top-description border-bottom">展示动画</view>
        <button type="primary" bindtap="rotateY">rotateY</button>
    </view>
</view>
```
* 在 js 文件中

```js
Page({
    data:{ },
    onReady() {
      this.animation = swan.createAnimation({
        transformOrigin: "50% 50%",
        duration: 1000,
        timingFunction: "ease",
        delay: 0})
    },
    rotateY() {
      this.animation.rotateY(Math.random() * 720 - 360).step()
      this.setData({animation: this.animation.export()})
    }
});
```
