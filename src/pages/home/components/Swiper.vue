<template>
  <div class="wrapper">
   <swiper :options="swiperOption">
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img class='swiper-img' :src="item.imgUrl" alt="">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-20/7426115.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-20/41983282.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
      background #ffffff !important
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 25.25%
    background #cccccc
    .swiper-img
      width 100%
</style>
