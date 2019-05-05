


<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div>
    <div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div><div class="icon">
      <div class="icon-img">
        <img
          class="icon-img-conntent"
          src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png"
        >
      </div>
      <p class="icon-desc">景点门票</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="stylus" scoped>
@import '~@/assets/veribles.styl';

.icons {
  overflow: hidden;
  height: 0;
  padding-bottom: 50%; // 撑起高度 是宽的一半

  .icon {
    position: relative; // 绝对定位
    overflow: hidden;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%; // 相当于宽度的25%

    .icon-img {
      position: absolute; // 相对定位
      top: 0;
      left: 0;
      right: 0;
      bottom: 1.4rem;
      box-sizing: border-box;
      padding: 0.4rem;

      .icon-img-conntent {
        height: 100%;
        // 居中
        display: block;
        margin: 0 auto;
      }
    }

    .icon-desc {
      position: absolute; // 相对定位
      left: 0;
      right: 0;
      bottom: 0;
      height: 1.4rem;
      line-height: 0.44rem;
      text-align: center;
      color: $darkTextColor;
    }
  }
}
</style>
