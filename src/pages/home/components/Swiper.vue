<template>
<div class="wrapper">
  <swiper :options="swiperOptions">
    <swiper-slide v-for='item of swiperList' :key="item.id">
      <img class="swiper-img"
        :src="item.imgUrl"
      />
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/p/tts3/1607/d7/59e865a21297c89a.jpg_r_640x420x95_173c5d6f.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/p/tts0/1607/5a/f9d0cf7ce2564c9a.jpg_r_640x420x95_c5cbc242.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/p/tts5/1607/ab/c609e95fc86cfa9a.jpg_r_640x420x95_3aa61e19.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width :100%
    height :0
    overflow :hidden
    padding-bottom :31.25%
    background :#eee
    .swiper-img
      width :100%
</style>
