<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" :alt="item.title">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/68207900.jpg',
          title: '形势变化',
          desc: '达不成补偿代表处的'
        },
        {
          id: '0002',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/49085717.jpg',
          title: 'CDC上的的程度',
          desc: '产地四川省杰出的成就'
        },
        {
          id: '0003',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/53111634.jpg',
          title: '从当初的不错',
          desc: '从成都市成都市CDC的'
        },
        {
          id: '0004',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/15525469.jpg',
          title: '差不多删除',
          desc: 'CDC但是传递出多层次的长度'
        },
        {
          id: '0005',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/73368647.jpg',
          title: '才不会代表处代表',
          desc: '导出到处都是CDC对策'
        },
        {
          id: '0006',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/31588707.jpg',
          title: '咯空哦空',
          desc: '都差不多吧成都成都CDC'
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
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #cccccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #ffffff
</style>
