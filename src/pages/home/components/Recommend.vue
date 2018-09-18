<template>
  <div>
    <div class="recommend-title">本周热门榜单</div>
    <ul>
      <li
        v-for="item of recommendList"
        class="item border-bottom"
        :key="item.id"
      >
        <img :src="item.imgUrl" class="item-img" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-botton">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: '武隆天坑地缝国家地质公园',
        desc: '5A级景区，喀斯特地貌，世界自然遗产',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg'
      }, {
        id: '0002',
        title: '武隆天坑地缝国家地质公园',
        desc: '5A级景区，喀斯特地貌，世界自然遗产',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg'
      }, {
        id: '0003',
        title: '武隆天坑地缝国家地质公园',
        desc: '5A级景区，喀斯特地貌，世界自然遗产',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg'
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
  .item
    display: flex
    height: 2rem
    .item-img
      width: 1.8rem
      height: 1.8rem
      padding: 0.1rem
    .item-info
      flex: 1
      padding: 0.1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        color: #000
        ellipsis()
      .item-desc
        margin-top: .1rem
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-botton
        font-size: .26rem
        background: #ff8824
        color: #fff
        border-radius: .06rem
        line-height: .4rem
        margin-top: .2rem
        padding: 0 .06rem
</style>
