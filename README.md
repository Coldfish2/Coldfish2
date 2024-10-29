## Henry 👋

<template>
    <div>
      <!-- 最外层的盒子 -->

      <div class="outerBox">
        <!-- 第一大块 -->
        <!-- 左边整体的内容 -->
        <div class="dateBox">
          <h2>2021/12/31</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容事件的详细内容事件的详细内容事件的详细内容事件的详细内容</ul>
          </div>
        </div>
        <!-- 右边整体的内容 -->
        <div class="dateLeftBox" style="top: 120px;">
          <h2>2021/12/25</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>
        </div>

        <!-- 第二大块 -->
        <!-- 左边整体的内容 -->
        <div class="dateBox" style="top: 240px;">
          <h2>2021/12/23</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>

        </div>
        <!-- 右边整体的内容 -->
        <div class="dateLeftBox" style="top: 360px;">
          <h2>2021/12/13</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>
        </div>

        <!-- 第三大块 -->
        <!-- 左边整体的内容 -->
        <div class="dateBox" style="top: 480px;">
          <h2>2020/12/23</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>

        </div>
        <!-- 右边整体的内容 -->
        <div class="dateLeftBox" style="top: 600px;">
          <h2>2020/05/14</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>
        </div>

        <!-- 第四大块 -->
        <!-- 左边整体的内容 -->
        <div class="dateBox" style="top: 720px;">
          <h2>2020/12/23</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>

        </div>
        <!-- 右边整体的内容 -->
        <div class="dateLeftBox" style="top: 840px;">
          <h2>2020/05/14</h2>
          <div>
            <p>发生的事件</p>
            <ul>事件的详细内容</ul>
          </div>
        </div>
      </div>

    </div>

</template>

  <script>
  export default {};
  </script>

  <style scoped>
  .outerBox {
    /* 竖线样式 高度根据事件的多少调整*/
    width: 5px;
    height: 900px;
    background: rgb(221, 221, 221);
    margin: 40px auto;
    position: relative;
    -webkit-animation: heightSlide 2s linear;
  }
  
  @-webkit-keyframes heightSlide {
    /* 竖线的动画效果：以百分比来规定改变发生的时间，0% 是动画的开始时间，100% 动画的结束时间 */
    0% {
      height: 0;
    }
  
    100% {
      height: 900px;
    }
  }
  
  .outerBox:after {
    /* 竖线末尾文字样式 */
    content: "未完待续";
    width: 100px;
    color: rgb(84, 84, 85);
    position: absolute;
    margin-left: -48px;
    text-align: center;
    bottom: -30px;
    -webkit-animation: showIn 5.5s ease;
  }
  
  .outerBox .dateBox,
  .outerBox .dateLeftBox {
    /* 球球的样式 */
    position: absolute;
    margin-left: -4px;
    margin-top: -10px;
    width: 13px;
    height: 13px;
    border-radius: 50%;
    border: 4px solid rgb(221, 221, 221);
    background: rgb(31, 122, 252);
    -webkit-transition: all 0.5s;
    -webkit-animation: showIn ease;
  }
  
  .outerBox .dateBox:nth-child(1) {
    /* 第一个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 1s;
  }
  
  .outerBox .dateLeftBox:nth-child(2) {
    /* 第二个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 1.5s;
  }
  
  .outerBox .dateBox:nth-child(3) {
    /* 第三个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 2s;
  }
  
  .outerBox .dateLeftBox:nth-child(4) {
    /* 第四个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 2.5s;
  }
  
  .outerBox .dateBox:nth-child(5) {
    /* 第五个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 3s;
  }
  
  .outerBox .dateLeftBox:nth-child(6) {
    /* 第六个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 3.5s;
  }
  
  .outerBox .dateBox:nth-child(7) {
    /* 第七个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 4s;
  }
  
  .outerBox .dateLeftBox:nth-child(8) {
    /* 第八个事件 设置动画在几秒内完成 */
    -webkit-animation-duration: 4.5s;
  }
  
  @-webkit-keyframes showIn {
    /* 球球、竖线、左右的模块的动画 */
    0%,
    70% {
      opacity: 0;
    }
  
    100% {
      opacity: 1;
    }
  }
  
  .outerBox .dateBox h2,
  .outerBox .dateLeftBox h2 {
    /* 日期的样式 */
    position: absolute;
    margin-left: -120px;
    margin-top: 3px;
    color: rgb(84, 84, 85);
    font-size: 14px;
    cursor: pointer;
    /* -webkit-animation: showIn 3s ease; */
  }
  
  .outerBox .dateLeftBox h2 {
    /* 右边日期的样式 */
    margin-left: 60px;
    width: 100px;
  }
  
  .outerBox .dateBox:hover,
  .outerBox .dateLeftBox:hover {
    /* 触摸事件后球球的样式 */
    border: 4px solid rgb(195, 195, 195);
    background: rgb(143, 189, 253);
    box-shadow: 0 0 2px 2px rgba(255, 255, 255, 0.4);
  }
  
  .outerBox .dateBox div,
  .outerBox .dateLeftBox div {
    /* 左右事件的样式 */
    position: absolute;
    top: 50%;
    margin-top: -10px;
    left: 50px;
    width: 300px;
    height: 22px;
    border: 2px solid rgb(84, 84, 85);
    border-radius: 6px;
    z-index: 2;
    overflow: hidden;
    cursor: pointer;
    /* -webkit-animation: showIn 5s ease; */
    -webkit-transition: all 0.5s;
  }
  
  .outerBox .dateLeftBox div {
    /* 左边事件的样式 */
    left: -337px;
  }
  
  .outerBox .dateBox div:hover,
  .outerBox .dateLeftBox div:hover {
    /* 触摸事件后的高度 */
    height: 68px;
  }
  
  .outerBox .dateBox div p,
  .outerBox .dateLeftBox div p {
    /* 左右事件的字体样式 */
    color: rgb(84, 84, 85);
    font-weight: bold;
    text-align: center;
  }
  
  .outerBox .dateBox:before,
  .outerBox .dateLeftBox:before {
    /* 右边事件的角标样式 */
    content: "";
    position: absolute;
    top: -4px;
    left: 37px;
    width: 0px;
    height: 0px;
    border: 7px solid transparent;
    border-right: 7px solid rgb(84, 84, 85);
    z-index: -1;
    -webkit-animation: showIn 5s ease;
  }
  
  .outerBox .dateLeftBox:before {
    /* 左边事件的角标样式 */
    left: -38px;
    border: 7px solid transparent;
    border-left: 7px solid rgb(84, 84, 85);
  }
  
  .outerBox .dateBox div ul,
  .outerBox .dateLeftBox div ul {
    /* 左右事件触摸展开后内容的样式 */
    list-style: none;
    width: 300px;
    padding: 4px;
    border-top: 2px solid rgb(84, 84, 85);
    color: rgb(84, 84, 85);
    font-size: 14px;
  }
  </style>
