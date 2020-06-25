<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl"/>
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
    data(){
        return {
            recommendList:[
                {
                    id:'0001',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'海洋馆',
                    desc:'世界最大的海洋馆'
                },
                {
                    id:'0002',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'东方明珠',
                    desc:'世界最大的电视塔'
                },
                {
                    id:'0003',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'上海科技馆',
                    desc:'世界最大的科技馆'
                },
                {
                    id:'0004',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'世纪公园',
                    desc:'世界最大的公园'
                },
                {
                    id:'0005',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'野生动物园',
                    desc:'世界最大的野生动物园'
                },
                {
                    id:'0006',
                    imgUrl:'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
                    title:'滴水湖',
                    desc:'世界最大的湖'
                }
            ]
        }
    }
}
</script>
<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
        line-height .8rem
        background :#eee
        text-indent :.2rem
        margin-top :.2rem
    .item-img-wrapper
        height :0
        overflow :hidden
        padding-bottom :33.9%
    .item-img
        width :100%
    .item-info
        padding :.1rem
        .item-title
            line-height :.54rem
            font-size :.32rem
            ellipsis()
        .item-desc
            ling-height :.4rem
            color :#ccc
            ellipsis()
</style>