<template>
  <div>
    <div class="title">
      <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png">
      <div>热门推荐</div>
    </div>
    <ul>
      <li class="item" v-for="(item) in itemList" :key="item.id">
        <img
          class="item-img"
          :src="item.imgUrl"
        >
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">{{item.button}}</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
      return {
          itemList:[{
              id:"001",
              imgUrl:"http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg",
              title:"长隆野生动物世界",
              desc:"浪漫大连首站，浪漫的海洋公园主题",
              button:"查看详情"
          },
          {
              id:"002",
              imgUrl:"http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg",
              title:"长隆野生动物世界",
              desc:"浪漫大连首站，浪漫的海洋公园主题",
              button:"查看详情"
          },
          {
              id:"003",
              imgUrl:"http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg",
              title:"长隆野生动物世界",
              desc:"浪漫大连首站，浪漫的海洋公园主题",
              button:"查看详情"
          }]
      }
  },
};
</script>


<style lang="stylus" scoped>
@import '~@/assets/veribles.styl';
.title {
  margin-top: 0.4rem;
  line-height: 1.6rem;
  background-color: #eee;
  text-indent: 0.4rem; // 第一行缩进多少
  display: flex;
}

.title-img {
  height: 0.93rem;
  width: 0.93rem;
  margin-top: 0.3rem;
  margin-left: 0.3rem;
  margin-right: 0;
}

.item {
  height: 8.625rem;
  display: flex;
  overflow: hidden;

  .item-img {
    width: 6.25rem;
    height: 6.25rem;
    padding: 0.625rem;
  }

  .item-info {
    flex: 1;
    padding: 0.625rem;
    min-width: 0;  //给定元素设置最小宽度
    

    .item-title {
      line-height: 1.94rem;
      font-size: 1.13rem;
      // 超出文字部分用...代替
      ellipsis();
    }

    .item-desc {
      line-height: 1.75rem;
      font-size: 0.8rem;
      color: #ccc;
      // 超出文字部分用...代替
      overflow: hidden;
      ellipsis();
    }

    .item-button {
      padding: 0.4rem;
      background: #ff9300;
      border-radius: 0.6rem;
    }
  }
}
</style>
