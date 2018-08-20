<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page, index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div class="icon-img">
                        <img :src="item.imgUrl" class="icon-img-content">
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data () {
        return {
            iconsList: [{
                id: '0001',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t17725/156/1767366877/17404/f45d418b/5ad87bf0N66c5db7c.png',
                desc: '生鲜超市'
            },{
                id: '0002',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t21658/347/221358098/7461/f86e6f74/5b03b170Nc9e0ec7c.png',
                desc: '全球购'
            },{
                id: '0003',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t23860/262/2268924264/14634/cb8f58f0/5b799949N6f75a2f0.png',
                desc: '京东超市'
            },{
                id: '0004',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t17725/156/1767366877/17404/f45d418b/5ad87bf0N66c5db7c.png',
                desc: '生鲜超市'
            },{
                id: '0005',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t21658/347/221358098/7461/f86e6f74/5b03b170Nc9e0ec7c.png',
                desc: '全球购'
            },{
                id: '0006',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t23860/262/2268924264/14634/cb8f58f0/5b799949N6f75a2f0.png',
                desc: '京东超市'
            },{
                id: '0007',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t17725/156/1767366877/17404/f45d418b/5ad87bf0N66c5db7c.png',
                desc: '生鲜超市'
            },{
                id: '0009',
                imgUrl: 'https://m.360buyimg.com/mobilecms/jfs/t23860/262/2268924264/14634/cb8f58f0/5b799949N6f75a2f0.png',
                desc: '京东超市'
            }]
        }
    },
    computed: {
        pages () {
            const pages = []
            this.iconsList.forEach((item, index) => {
                const page = Math.floor(index / 8)
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    @import '~styles/mixins.styl'
    .icons >>> .swiper-container
        height : 0
        padding-bottom : 50%
    .icon
        overflow : hidden
        float : left
        width : 25%
        height : 0
        padding-bottom : 25%
        position : relative
        .icon-img
            position : absolute
            top : 0
            left : 0
            right : 0
            bottom : .44rem
            box-sizing : border-box
            padding : .1rem
            .icon-img-content
                display : block
                margin : 0 auto
                height : 100%
        .icon-desc
            position : absolute
            bottom : 0
            left : 0
            right : 0
            height : .44rem
            line-height : .44rem
            text-align : center
            color : $darkTextColor
            ellipsis()
</style>


