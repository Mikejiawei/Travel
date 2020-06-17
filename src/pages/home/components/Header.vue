<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe659;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      请输入内容
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont">&#xe65a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from "vuex";
export default {
  name: "HomeHeader",
  computed: {
    ...mapState(["city"])
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/variable.styl';

.header {
  display: flex;
  line-height: $headerHeight;
  background: $bgColor;
  color: #ffffff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      padding-top: 0.1rem;
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    align-self: center;
    line-height: 0.54rem;
    padding-left: 0.2rem;
    margin-top: 0.12rem;
    margin-left: 0.2rem;
    background: #ffffff;
    color: #cccccc;
    border-radius: 0.1rem;
  }

  .header-right {
    padding: 0.1rem;
    min-width: 1.04rem;
    float: right;
    text-align: center;
    color: #fff;

    .arrow-icon {
      margin-left: -0.04rem;
      font-size: 0.24rem;
    }
  }
}
</style>
