<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe659;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      请输入内容
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe65a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>

<style lang="stylus" scoped>
@import "~styles/variable.styl"
.header
  display flex
  line-height .86rem
  background $bgcolor
  color #ffffff
  .header-left
    width .64rem
    float left
    .back-icon
      padding-top 0.1rem
      text-align center
      font-size 0.4rem
  .header-input
    flex 1
    align-self center
    line-height .54rem
    padding-left .2rem
    margin-top .12rem
    margin-left .2rem
    background #ffffff
    color #cccccc
    border-radius .1rem
  .header-right
    padding-top 0.1rem
    width 1.24rem
    float right
    text-align center
</style>
