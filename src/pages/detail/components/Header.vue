<template>
<div>
    <router-link tag="div" to="/" class="header-abs" v-show="showAbs">
         <div class="iconfont header-abs-back">&#xe6db;</div>
    </router-link>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
        <router-link to="/">
            <div class="iconfont header-fixed-back">&#xe6db;</div>
        </router-link>
        景点详情
    </div>
</div>
</template>
<script>
import CommonGallary from "common/gallary/Gallary"
export default {
    name:'DetailHeader',
    data () {
        return {
            showAbs:true,
            opacityStyle:{
                opacity:0
            }
        }
    },
    methods:{
        handleScroll() {
            const top=document.documentElement.scrollTop
            if (top>60){
                let opacity=top / 140 
                opacity = opacity>1?1:opacity
                this.opacityStyle={opacity}
                this.showAbs=false
            }else{
                this.showAbs=true
            }
            
        }
    },
    activated () {
        window.addEventListener('scroll',this.handleScroll)
    },
    deactivated () {
        window.removeEventListener('scroll',this.handleScroll)
    }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header-abs
    position absolute
    left .2rem
    top .2rem
    width .8rem
    height .8rem
    line-height .8rem
    text-align center
    border-radius .4rem
    background rgba(0,0,0,.8)
    .header-abs-back
        color #ffffff
        font-size .4rem
.header-fixed
    z-index 2
    position fixed  
    top 0
    left 0
    right 0  
    padding-top .22rem
    height .6rem
    line-height $headerHeight
    text-align center
    color #fff
    background-color $bgColor
    font-size .32rem
    .header-fixed-back
        position absolute
        top 0
        left 0
        padding-top .2rem
        width .64rem
        text-align center
        font-size .4rem
        color #fff
</style>