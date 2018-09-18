<template>
  <div>
    <div class="icons">
      <swiper :options="swiperOption">
        <swiper-slide
          v-for="(page, index) of pages"
          :key="index"
        >
          <div
            class="icon"
            v-for="item of page"
            :key="item.id"
          >
            <div class="icon-img">
              <img class="icon-img-content" :src="item.imgUrl" />
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
export default{
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        autoplay: false
      },
      iconList: [{
        id: '0001',
        desc: '景点门票',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
      },
      {
        id: '0002',
        desc: '景区直通车',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png'
      },
      {
        id: '0003',
        desc: '重庆必游',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png'
      },
      {
        id: '0004',
        desc: '夏日玩水',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png'
      },
      {
        id: '0005',
        desc: '一日游',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png'
      },
      {
        id: '0006',
        desc: '两江夜游',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png'
      },
      {
        id: '0007',
        desc: '神秘武隆',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png'
      },
      {
        id: '0008',
        desc: '游乐场',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png'
      },
      {
        id: '0009',
        desc: '全部玩乐',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
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
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons >>> .swiper-pagination-bullet
    width: .12rem;
    height: .12rem;
    margin: 0 4px;
  .icons >>> .swiper-pagination
    bottom: .12rem;
    line-height: .12rem;
  .icons
    margin-top: .2rem
    overflow: hidden
    height: 0
    padding-bottom: 50%
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        right: 0
        left: 0
        bottom: .5rem
        box-sizing: border-box
        padding-top: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
    .icon-desc
      position: absolute
      right: 0
      left: 0
      bottom: 0
      line-height: .4rem
      text-align: center
      color: $darkTextColor
      box-sizing: border-box;
      padding-bottom: .1rem;
      ellipsis()
</style>
