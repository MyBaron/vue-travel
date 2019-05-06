<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icon :iconList="iconList"></home-icon>
    <home-recommend :recommendList="recommendList"></home-recommend>
  </div>
</template>

<script>
import HomeHeader from "./components/Header.vue";
import HomeSwiper from "./components/Swiper.vue";
import HomeIcon from "./components/Icon.vue";
import HomeRecommend from "./components/Recommend.vue";
import axios from "axios";

export default {
  name: "Home",
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper: HomeSwiper,
    HomeIcon: HomeIcon,
    HomeRecommend: HomeRecommend
  },
  data() {
    return {
      city: "",
      iconList: [],
      swiperList: [],
      recommendList: []
    };
  },
  methods: {
    getHomeInfo() {
      axios.get("/data/index.json").then(this.getHomeInfoSucc);
    },
    getHomeInfoSucc(res) {
      const re = res.data;
      if (re.ret && re.data) {
        const data = re.data;
        this.city = data.city;
        this.iconList = data.iconList;
        this.swiperList = data.swiperList;
        this.recommendList = data.recommendList;
      }
    }
  },
  mounted() {
    this.getHomeInfo();
  }
};
</script>
