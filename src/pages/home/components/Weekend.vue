<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id" >
      <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
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
    return{
      recommendList : [{
      id: '0001',
      imgUrl: 'http://img1.qunarzz.com/sight/source/1505/3b/90c6e4c0a3d7bf.jpg_r_640x214_5f7b77f9.jpg',
      title: '荷兰花海',
      desc: '盐城本月收藏Top5╰(￣▽￣)╭',
    }, {
      id: '0002',
      imgUrl: 'http://img1.qunarzz.com/sight/source/1505/3b/90c6e4c0a3d7bf.jpg_r_640x214_5f7b77f9.jpg',
      title: '麋鹿保护区',
      desc: '这里特别受欢迎哟(๑‾ ꇴ ‾๑)',
    }, {
      id: '0003',
      imgUrl: 'http://img1.qunarzz.com/sight/source/1505/3b/90c6e4c0a3d7bf.jpg_r_640x214_5f7b77f9.jpg',
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
  .item-img-wrapper
    overflow: hidden
    height : 0
    padding-bottom: 33.9%
    .item-img
        width :100%
  .item-info  
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
</style>

