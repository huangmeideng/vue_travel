<template>
  <div>
    <div class="item" v-for="(item, index) in list" :key="index">
      <div class="item-title border-bottom">
        <span class="iconfont item-title-icon">&#xe653;</span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .item-title
    line-height .8rem
    font-size .32rem
    padding 0 .2rem
    font-size .3rem
    .item-title-icon
      position relative
      left .01rem
      top .01rem
      color $bgColor
  .item-children
    padding 0 .2rem
</style>
