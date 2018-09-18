<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li
        v-for="item of recommendList"
        class="item"
        :key="item.id"
      >
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img" />
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
export default{
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: '重庆大美古镇',
        desc: '行走重庆最美古镇，让你瞬间穿越千年',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/48/f117e9b3bf582a.jpg_r_640x214_b8145711.jpg'
      }, {
        id: '0001',
        title: '重庆大美古镇',
        desc: '行走重庆最美古镇，让你瞬间穿越千年',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/48/f117e9b3bf582a.jpg_r_640x214_b8145711.jpg'
      }, {
        id: '0001',
        title: '重庆大美古镇',
        desc: '行走重庆最美古镇，让你瞬间穿越千年',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/48/f117e9b3bf582a.jpg_r_640x214_b8145711.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #f0f0f0
    text-indent: .2rem
  .item-img-wrapper
    height: 0
    padding-bottom: 36%
    overflow: hidden
    .item-img
      width: 100%
  .item-info
    padding: 0.2rem
    min-width: 0
    .item-title
      line-height: .4rem
      font-size: .32rem
      color: #000
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
