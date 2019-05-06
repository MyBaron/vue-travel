<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入景点/城市/游玩主题
    </div>
    <router-link to="/City">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>


<script>
export default {
  name: "HomeHeader",
  props: ["city"]
};
</script>


<style lang="stylus" scoped>
@import '~@/assets/veribles.styl';

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
  color: #fff;

  .arrow-icon {
    margin-left: -0.2rem;
    font-size: 0.4rem;
  }
}
</style>

