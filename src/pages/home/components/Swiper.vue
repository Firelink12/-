<template>
<div class="wrapper">
     <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img  class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
   
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>

export default {
    name:'HomeSwiper',
    data () {
        return{
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
            id:'0001',
            imgUrl:'https://imgs.qunarzz.com/piao/fusion/1609/72/0ecfb6185eef8f02.jpg_890x330_7e0538e4.jpg'
        },{
            id: '0002',
            imgUrl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/e918899bb89151d054ee9c9992dd97f1.jpg_890x330_70f81240.jpg'
        }]
        }
        
    }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff  
.wrapper >>> .swiper-pagination-bullets
    bottom 26px
.wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%
    background-color: #eee
    .swiper-img
        width:100%
  

</style>