<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入景点/城市/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>


<script>
export default {
  name: "HomeHeader"
};
</script>


<style lang="stylus" scoped>
@import "~@/assets/veribles.styl";
.header {
  display: flex;
  line-height: 1.96rem;
  background: $bgColor;
  color: #fff;
}

.header-left {
  width: 2.4rem;
  float: left;

  .back-icon {
    text-align: center;
    font-size: 1rem;
  }
}

.header-input {
  flex: 1;
  height: 1.56rem;
  padding-left: 0.4rem;
  line-height: 1.4rem;
  margin-top: 0.24rem;
  margin-bottom: 0.24rem;
  margin-left: 0.4rem;
  background: #fff;
  border-radius: 0.2rem;
  color: #ccc;
}

.header-right {
  width: 5.12rem;
  float: right;
  text-align: center;

  .arrow-icon {
    margin-left: -0.2rem;
    font-size: 0.4rem;
  }
}
</style>

