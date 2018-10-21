<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" :alt="item.desc">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [
        {
          id: '0001',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/89429970.jpg',
          desc: '景点门票'
        },
        {
          id: '0002',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/84074220.jpg',
          desc: '一日游'
        },
        {
          id: '0003',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/81270080.jpg',
          desc: '自助游'
        },
        {
          id: '0004',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/98335119.jpg',
          desc: '酒店'
        },
        {
          id: '0005',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/39456985.jpg',
          desc: '美食'
        },
        {
          id: '0006',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/40823563.jpg',
          desc: '热门景点'
        },
        {
          id: '0007',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/10758567.jpg',
          desc: '自然风光'
        },
        {
          id: '0008',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/56830501.jpg',
          desc: '科技馆'
        },
        {
          id: '0009',
          imgUrl: 'http://ozy3pax09.bkt.clouddn.com/18-10-21/69189710.jpg',
          desc: '全部'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  @import '~styles/mixins.styl';
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    margin-top .1rem
    .icon
      position relative
      overflow hidden
      float left
      width 25%
      height 0
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        .icon-img-content
          display block
          margin 0 auto
          height 100%
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        text-align center
        color $darkTextColor
        ellipsis()
</style>
