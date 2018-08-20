<template>
    <div>
        <div class="recommend-title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" alt="" class="item-img">
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
        return {
            recommendList: [{
                id: '0001',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
                title: '金海湖风景区',
                desc: '浪漫的风景乐园，共享和谐人生'
            },{
                id: '0002',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
                title: '金海湖风景区',
                desc: '浪漫的风景乐园，共享和谐人生'
            },{
                id: '0003',
                imgUrl: 'http://img1.qunarzz.com/sight/source/1606/85/c6b6bad1b977e.jpg_r_640x214_5c638941.jpg',
                title: '金海湖风景区',
                desc: '浪漫的风景乐园，共享和谐人生'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .recommend-title
        margin-top : .2rem
        line-height : .8rem
        background : #eee
        text-indent : .5rem
    .item-img-wrapper
        overflow : hidden
        height : 0
        padding-bottom : 33.9%
    .item-img
        width : 100%
        
    .item-info
        padding : .1rem
        .tem-title
            line-height : .54rem
            font-size : .32rem
            ellipsis()
        .item-desc
            line-height : .4rem
            color : #ccc
            ellipsis()
</style>


