<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe6db;</div>
    </div>
    <div class="header-input">
       <span class="iconfont">&#xe6e1;</span>输入城市景点/游玩/主题</div>
    <div class="header-right">{{this.city}}
      <span class="iconfont arrow-icon">&#xe69b;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader",
  props:{
    city:String
  }
};
</script>

<style lang="stylus" scoped>
/* 1rem=html font-size =50px */
@import '~styles/varibles.styl';
.header {
  display: flex;
  line-height: 0.86rem;
  background: $bgColor;
  color: #fff;
}

.header-left {
  width: 0.64rem;
  float: left;
}
.back-icon{
  text-align center
  font-size .5rem
}

.header-right {
  width: 1.24rem;
  float: right;
  text-align: center;
}
.arrow-icon{
  font-size:.24rem
  margin-left:-.04rem
}

.header-input {
  padding-left .2rem
  margin-top .12rem;
  line-height .62rem
  margin-left:.2rem
  flex: 1;
  background:#fff;
  border-radius .1rem;
  color:#ccc
  height .64rem
}
</style>