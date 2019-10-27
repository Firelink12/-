<template>
<div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key='item.id'>
            <div class="item-img-wrapper">
                <img class="item-img" :src='item.imgUrl' />
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
    name:'HomeWeekend',
    data () {
        return {
        recommendList:[{
            id:'0001',
            imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg',
            title: "美丽普陀山",
            desc:'人间仙境杭州，佛教圣地普陀山等你来玩！在这里静心接收佛家的洗礼，用心感受佛文化'
        },{
            id:'0002',
            imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/b2/5e303795b9aadf.jpg_r_640x214_50ec7a9c.jpg',
            title: "宁波必打卡",
            desc:'宁波美腻到骨子里，不可言喻'
        },{
            id:'0003',
            imgUrl: 'https://imgs.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
            title: "温州动人秋色",
            desc:'细数温州那些美到陶醉的赏秋地'
        },]
    }
    }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
    .title
        margin-top .2rem
        line-height .8rem
        background #eee
        text-indent .2rem
    .item-img-wrapper
        overflow hidden
        height 0
        padding-bottom 33.9%
        .item-img
           width 100%
    .item-info
        padding .1rem
        .item-title
            line-height .54rem
            font-size .32rem
            ellipsis()
        .item-desc
            line-height .4rem
            color #ccc
            ellipsis()

</style>