<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
  </div>
</template>

<script>
import CityHeader from "./components/Header.vue";
import CitySearch from "./components/Search.vue";
export default {
  name: "city",
  components: {
    CityHeader,
    CitySearch
  }
};
</script>

<style scoped>
</style>
