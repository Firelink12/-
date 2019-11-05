<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1701/6c/6c5e1f8fa365adada3.img.png_600x330_51efe2f1.png" /> 
        <div class="banner-info">
            <div class="banner-title">宁波方特东方神画</div>
            <div class="banner-number banner-icon"><span class="iconfont" >&#xe6e1;</span>39</div>
        </div>
    </div>
    <common-gallary @close="handleGallaryClose" :imgs="imgs" v-show="showGallary"></common-gallary>
</div>

</template>
<script>
import CommonGallary from "common/gallary/Gallary"
export default {
    name:'DetailBanner',
    components:{
        CommonGallary
    },
    data () {
        return {
            showGallary:false,
            imgs:['http://img1.qunarzz.com/sight/p0/1701/6c/6c5e1f8fa365adada3.img.png_r_800x800_bcbc8092.png','http://img1.qunarzz.com/sight/p0/1808/d1/d137655f0353c42ea3.img.png_r_800x800_1f755d3f.png']
        }
    },
    methods:{
        handleBannerClick () {
            this.showGallary=true
        },
        handleGallaryClose () {
            this.showGallary=false
        }
    }
}
</script>
<style lang="stylus" scoped>
.banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
        width 100%
    .banner-info
        display flex
        position absolute
        left 0
        right 0
        bottom 0
        line-height .6rem
        color #fff
        background-image linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
        .banner-title
            flex 1
            font-size .32rem
            padding 0 .2rem
        .banner-number
            height .32rem
            margin-top .14rem
            padding 0 .4rem
            line-height .32rem
            border-radius .2rem
            background rgba(0, 0, 0, .8)
            font-size .24rem
            .banner-icon
                font-size .24rem

</style>