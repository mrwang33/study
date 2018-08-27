<template>
  <div class="icon-container">
    <div class="icon-content">
      <div class="icon-img">
        <img class="icon-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" />
      </div>
      <p class="icon-desc">景点门票</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  @import '~@@/variables.styl'

  .icon-container
    overflow : hidden
    height : 0
    width : 100%
    padding-bottom : 50%
    .icon-content
      position : relative
      float : left
      height : 0
      width : 25%
      overflow : hidden
      padding-bottom : 25%
      .icon-img
        position : absolute
        top : 0
        left : 0
        right : 0
        bottom : .44rem
        box-sizing : border-box
        padding : .1rem
        .icon-img-content
          display: block /**将img定义为块级元素,为了使margin有效**/
          margin: 0 auto /**左右上下居中**/
          height: 100%   /**图片完整显示 不拉伸**/
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color : $darkTextColor
</style>
