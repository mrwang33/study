<template>
  <div class="header">
    <div class="header-left">返回</div>
    <div class="header-center"></div>
    <div class="header-right">地点</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
.header
  display : flex
  background-color : #66ccff
  line-height : .84rem
  .header-left
    float : left
    color : #ffffff
    width : .64rem
  .header-center
    flex : 1
    background-color : #ffffff
    border-radius : .1rem
    margin-top : .12rem
    margin-bottom : .12rem
    line-height : 60rem
  .header-right
    width : 1.24rem
    float : right
    color : #ffffff
    text-align : center
</style>
