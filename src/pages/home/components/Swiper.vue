<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
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
        pagination: ".swiper-pagination",
        loop: true
      },
      swiperList: [
        {
          id: "0001",
          imgUrl:
            "https://images.pexels.com/photos/1430677/pexels-photo-1430677.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
        },
        {
          id: "0002",
          imgUrl:
            "https://images.pexels.com/photos/386025/pexels-photo-386025.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullets
  bottom 20px
  .swiper-pagination-bullet-active
    background #fff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 30%
  background #eee
  .swiper-img
    height 2.5rem
    width 100%
</style>
