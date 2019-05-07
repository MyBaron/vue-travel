<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或者拼音">
  </div>
</template>


<script>
export default {
  name: "CitySearch"
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/veribles.styl';

.search {
  color: #fff;
  background: $bgColor;
  height: 2.2rem;
  padding: 0 0.4rem;

  .search-input {
    box-sizing: border-box;
    width: 100%;
    line-height: 1.8rem;
    text-align: center;
    border-radius: 0.32rem;
    padding: 0 0.2rem;
    color: #666;
  }
}
</style>
