<template>
  <div class="icon-container">
    <swiper :options="iconSwiperOption" ref="mySwiper">
      <swiper-slide v-for="(pageNum,index) in imgPage.pageSize" :key="index">
        <div class="icon-content" v-for="imgItem in imgPage.content[index]" :key="imgItem.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="imgItem.imgSrc" />
          </div>
          <p class="icon-desc">{{imgItem.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data: function () {
    return {
      imgList: [
        {
          id: '0001',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc: '景点门票'
        },
        {
          id: '0002',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc: '一日游'
        },
        {
          id: '0003',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc: '杭州必游'
        },
        {
          id: '0004',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          desc: '漂游'
        },
        {
          id: '0005',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
          desc: '夏日玩水'
        },
        {
          id: '0006',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png',
          desc: '西湖'
        },
        {
          id: '0007',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
          desc: '宋城'
        },
        {
          id: '0008',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
          desc: '汽车票'
        },
        {
          id: '0009',
          imgSrc:
            'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
          desc: '千岛湖'
        }
      ],
      iconSwiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    imgPage: function () {
      var page = {}
      page.pageSize = Math.floor(this.imgList.length / 8) + 1
      page.content = [page.pageSize]
      for (var i = 0; i < page.pageSize; i++) {
        var index = i * 8
        page.content[i] = []
        for (var j = index; j < index + 8; j++) {
          if (this.imgList[j]) {
            page.content[i].push(this.imgList[j])
          }
        }
      }
      return page
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@@/variables.styl';

.icons-container >>> .swiper-container {
  height: 0;
  padding-bottom: 25%;
}

.icon-container {
  overflow: hidden;
  height: 0;
  width: 100%;
  padding-bottom: 50%;

  .icon-content {
    position: relative;
    float: left;
    height: 0;
    width: 25%;
    overflow: hidden;
    padding-bottom: 25%;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-sizing: border-box;
      padding: 0.1rem;

      .icon-img-content {
        display: block; /* *将img定义为块级元素,为了使margin有效* */
        margin: 0 auto; /* *左右上下居中* */
        height: 100%; /* *图片完整显示 不拉伸* */
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      text-align: center;
      white-space: nowrap; /* *禁止文字换行* */
      overflow: hidden; /* *滚动条* */
      text-overflow: ellipsis; /* *字数太多以省略号展示* */
      color: $darkTextColor;
    }
  }
}
</style>
