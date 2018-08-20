<template>
    <div class="swiper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img :src="item.imgUrl" class="swiper-img">
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: '0001',
                imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/dujia_shuqi_banner_20180710.jpg'
            },{
                id: '0002',
                imgUrl: 'https://source.qunarzz.com/site/images/wap/home/recommend/iphoneplus/anquan_20180716.png'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .swiper >>> .swiper-pagination-bullet-active
        background : #fff
    .swiper
        overflow : hidden
        width : 100%
        height : 0
        padding-bottom : 24.5%
        background-color : #ccc
        .swiper-img
            width 100%
</style>


