<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    position: relative
    overflow: hidden
    height : $header-height
    line-height : $header-height
    text-align :center
    color : #fff
    background :$bgColor
    font-size : .35rem
    .header-back
      position: absolute
      top: 0
      left :0
      width :.64rem
      font-size :.4rem
      text-align : center
      color :#fff
</style>
