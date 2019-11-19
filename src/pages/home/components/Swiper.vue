<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swapper-img" :src="item.imgUrl"/>
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
      swiperList: [{
        id: '0001',
        imgUrl: 'https://dimg04.c-ctrip.com/images/zg0t1800000152y0m2769.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://dimg04.c-ctrip.com/images/zg0j170000011chb42B7F.jpg'
      }]
    }
  }
}
</script>

<style scoped lang="stylus">
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swapper-img
      width: 100%
</style>
