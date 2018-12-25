<template>
  <div class="foot-guide">
    <div class="guide-item" :class="{on:'/msite'===$route.path}" @click="goTo('/msite')">
      <span class="item-icon">
        <i class="iconfont icon-waimai"></i>
      </span>
      <span>外卖</span>
    </div>
    <div class="guide-item" :class="{on:'/search'===$route.path}" @click="goTo('/search')">
      <span class="item-icon" ref="">
        <i class="iconfont icon-search"></i>
      </span>
      <span>搜索</span>
    </div>
    <div class="guide-item" :class="{on:'/order'===$route.path}" @click="goTo('/order')">
      <span class="item-icon">
        <i class="iconfont icon-dingdan"></i>
      </span>
      <span>订单</span>
    </div>
    <div class="guide-item" :class="{on:'/profile'===$route.path}" @click="goTo('/profile')">
      <span class="item-icon">
        <i class="iconfont icon-geren"></i>
      </span>
      <span>我的</span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    methods: {
      goTo(path) {
        this.$router.replace(path)
      }
    }
  }
</script>

<style type="text/stylus" lang="stylus" rel="stylesheet/stylus" scoped>
  @import "../../common/stylus/mixins.styl"

  .foot-guide
    top-border-1px(#e4e4e4)
    position fixed
    z-index 100
    left 0
    right 0
    bottom 0
    background-color #fff
    width 100%
    height 50px
    display flex
    .guide-item
      flex: 1
      margin: 5px
      display: flex
      text-align: center
      flex-direction: column
      align-items: center
      color: #999999
      &.on
        color: #02a774
      span
        font-size 12px
        margin-top 2px
        margin-bottom 2px
        .iconfont
          font-size 22px
</style>
