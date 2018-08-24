<template>
  <div class="swiper-content">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg"/>
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="https://img1.qunarzz.com/piao/fusion/1808/fd/fddc5309111a0402.jpg_750x200_e7b93551.jpg"/>
      </swiper-slide>
      <swiper-slide>
        <img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1805/44/70b819ab2b3c02.jpg_750x200_fe9147c8.jpg"/>
      </swiper-slide>
      <!-- Optional controls -->
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
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .swiper-content >>> .swiper-pagination-bullet-active
    background : #ffffff
  .swiper-content
    overflow: hidden /**禁用滚动条**/
    width: 100%
    height: 0
    padding-bottom: 26% /**宽高比例**/
    background: #eee
    .swiper-img
      width : 100%
</style>
