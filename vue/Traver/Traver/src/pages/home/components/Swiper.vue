<template>
  <div class="swiper-content">
    <swiper :options="swiperOption" ref="mySwiper">
      <!-- slides -->
      <swiper-slide v-for="item in list" :key="item.id">
        <img class="swiper-img" :src="item.src"/>
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
      list: [{
        id: 1,
        src: 'http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg'
      }, {
        id: 2,
        src: 'https://img1.qunarzz.com/piao/fusion/1808/fd/fddc5309111a0402.jpg_750x200_e7b93551.jpg'
      }, {
        id: 3,
        src: 'http://img1.qunarzz.com/piao/fusion/1805/44/70b819ab2b3c02.jpg_750x200_fe9147c8.jpg'
      }],
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
