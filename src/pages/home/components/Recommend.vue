<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id" >
      <img class="item-img" :src="item.imgUrl"/>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-buttom">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return{
      recommendList : [{
      id: '0001',
      imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/40/40ba0ec721370c1.water.jpg_200x200_88739c03.jpg',
      title: '荷兰花海',
      desc: '盐城本月收藏Top5╰(￣▽￣)╭',
    }, {
      id: '0002',
      imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/07/df9f3341563c9c00afb84774fafde5ba.jpg_200x200_267feaf9.jpg',
      title: '麋鹿保护区',
      desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)',
    }, {
      id: '0003',
      imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/af/af8840c141c2a146a3.water.jpg_200x200_d9182e37.jpg',
      title: '大丰港动物园',
      desc: '富含国家一类保护动物及国外珍稀野生物种',
    }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/mixins.styl"
  .title
    margin-top : .2rem
    line-height : .8rem
    background : #eee
    text-indent : .2rem
  .item
    display: flex
    overflow: hidden
    height : 1.9rem
    .item-img
      width : 1.7rem
      height : 1.7rem
      padding : .1rem
    .item-info  
      flex : 1
      padding : .1rem
      min-width : 0
      .item-title
        line-height : .44rem
        font-size: .3rem
        ellipsis()
      .item-desc
        margin-top : .1rem
        line-height :.4rem
        color : #ccc
        ellipsis()
      .item-buttom
        line-height : .44rem
        margin-top : .16rem
        background : #ff9300
        padding :0 .2rem
        border-radius : .06rem
        color : #fff
        ellipsis()
</style>

