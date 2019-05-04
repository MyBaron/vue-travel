<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide v-for="(item) in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination"
        },
        autoplay: {
          delay: 1000,
          stopOnLastSlide: false,
          disableOnInteraction: true
        },
        loop: true
      },
      swiperList: [
        {
          id: "001",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/5daa78ddf9a3e3aca32195e079b9545d.jpg_750x200_3aeaa5c2.jpg"
        },
        {
          id: "002",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/2680ea76118c1fc8f5d44b4240c20275.jpg_750x200_42900395.jpg"
        }
      ]
    };
  }
};
</script>
<style lang="stylus" scoped>

// 修改子模块的样式
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}
.wrapper {
    // 撑起照片的高度
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.7%;
  background: #eee;
}

.swiper-img {
  width: 100%;
}
</style>
