<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1805/eb/eb135bb3494ace1fa3.img.jpg_600x330_c26b91e1.jpg"/>
      <div class="banner-info">
        <div class="banner-title">
          五江温泉城
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe650;</span>
          39
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
  
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs : ['http://img1.qunarzz.com/sight/p0/1805/3b/3b8088864ec18b52a3.img.jpg_r_800x800_b107cbda.jpg','http://img1.qunarzz.com/sight/p0/1805/1d/1dc6edbf1ab487a0a3.img.jpg_r_800x800_c236ad21.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      position: absolute
      display: flex
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color : #fff
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        margin-top: .14rem
        margin-right :.14rem
        padding: 0 .4rem
        line-height: .32rem
        height: .32rem
        border-radius: .2rem
        background: rgba(0,0,0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
