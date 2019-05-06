<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(item, index) in pages" :key="index">
        <div class="icon" v-for="(item) in item" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-conntent" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeIcon",
  data() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination"
        }
      }
    };
  },
  props: ["iconList"],
  computed: {
    pages: function() {
      const pages = [];
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8);
        //如果为空
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>

<style lang="stylus" scoped>
@import '~@/assets/veribles.styl';

// 修改子模块的样式
.icons >>> .swiper-pagination-bullet-active {
  background: blue;
}

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
      // 超出文字部分用...代替
      ellipsis();
    }
  }
}
</style>
