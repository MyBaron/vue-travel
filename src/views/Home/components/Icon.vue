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
      },
      iconList: [
        {
          id: "001",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        {
          id: "002",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "广州必游"
        },
        {
          id: "003",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
          desc: "动植游园"
        },
        {
          id: "004",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png",
          desc: "自然风光"
        },
        {
          id: "005",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png",
          desc: "珠江夜游"
        },
        {
          id: "006",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png",
          desc: "泡温泉"
        },
        {
          id: "007",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
          desc: "一日游"
        },
        {
          id: "008",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/184e261814a5d07a5d3d08cd29cf590d.png",
          desc: "长隆度假区"
        },
        {
          id: "009",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/c032ae43b15a3dac34b5e07bb0e46850.png",
          desc: "广州塔"
        },
        {
          id: "010",
          imgUrl:
            "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/bda58ffc3016edad84e656e8a94b0321.png",
          desc: "广州融创"
        }
      ]
    };
  },
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
