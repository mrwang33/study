<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-center">
      <span class="iconfont">&#xe632;</span>
      请输入城市/景点
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~@@/variables.styl'

.header
  display : flex
  background-color : $bgColor
  line-height : .84rem
  .header-left
    float : left
    color : #ffffff
    width : .64rem
    .back-icon
      margin-left : .1rem
      font-size : .18rem
  .header-center
    flex : 1
    background-color : #ffffff
    border-radius : .1rem
    margin-top : .12rem
    margin-bottom : .10rem
    padding-left : .1rem
    line-height : .62rem
    color : #C0C0C0
  .header-right
    width : 1.24rem
    float : right
    color : #ffffff
    text-align : center
</style>
