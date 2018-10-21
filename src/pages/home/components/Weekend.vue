<template>
  <div>
    <div class="title">周末去哪玩</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" :alt="item.title">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/39395797.jpg',
          title: '形势变化',
          desc: '达不成补偿代表处的'
        },
        {
          id: '0002',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/89869505.jpg',
          title: 'CDC上的的程度',
          desc: '产地四川省杰出的成就'
        },
        {
          id: '0003',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/85729453.jpg',
          title: '从当初的不错',
          desc: '从成都市成都市CDC的'
        },
        {
          id: '0004',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/52640519.jpg',
          title: '差不多删除',
          desc: 'CDC但是传递出多层次的长度'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
  .title
    margin-top .2rem
    line-height .8rem
    background #eeeeee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #cccccc
      ellipsis()
</style>
