<template>
  <div class="header">
    城市选择
    <router-link to="/">
    <div class="iconfont header-icon">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: "CityHeader"
};
</script>

<style  lang="stylus" scoped>
@import '~@/assets/veribles.styl';

.header {
  position: relative;
  overflow: hidden;
  height: 2.2rem;
  line-height: 2.2rem; // 行高
  text-align: center; // 居中
  color: #fff;
  background: $bgColor;
  font-size: 1rem;

  .header-icon {
    position: absolute;
    left: 0rem;
    top: 0rem;
    margin-left: 0.5rem;
    font-size: 1.2rem;
    text-align: center;
    width: 1.2rem;
    color: #fff;
  }
}
</style>
