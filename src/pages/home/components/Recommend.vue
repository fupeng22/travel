<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl"/>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'HomeRecommend',
    data(){
        return {
            recommendList:[
                {
                    id:'0001',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/2005/a9/a9411416ff215fe2a3.water.jpg_200x200_3110fb7b.jpg',
                    title:'海洋馆',
                    desc:'世界最大的海洋馆'
                },
                {
                    id:'0002',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/2005/82/8253605ce47e06eba3.water.jpg_200x200_ad135a76.jpg',
                    title:'东方明珠',
                    desc:'世界最大的电视塔'
                },
                {
                    id:'0003',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/1507/b3/b33a7caa457c0a52.img.jpg_200x200_fe73bd81.jpg',
                    title:'上海科技馆',
                    desc:'世界最大的科技馆'
                },
                {
                    id:'0004',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/2005/9e/9e643f96c84b5c2ea3.water.jpg_200x200_2a3eef5b.jpg',
                    title:'世纪公园',
                    desc:'世界最大的公园'
                },
                {
                    id:'0005',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/1412/9f/fbff2a5302c0ce906ef9b64159730f89.water.jpg_200x200_87806940.jpg',
                    title:'野生动物园',
                    desc:'世界最大的野生动物园'
                },
                {
                    id:'0006',
                    imgUrl:'https://imgs.qunarzz.com/sight/p0/2005/23/23c1b2b13230b966a3.water.jpg_200x200_f3a19805.jpg',
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
    .item
        overflow :hidden 
        display :flex
        height :1.9rem
        .item-img
            width :1.7rem
            height :1.7rem
            padding :.1rem
        .item-info
            flex :1
            padding :.1rem
            min-width :0
            .item-title
                line-height :.54rem
                font-size :.32rem
                ellipsis()
            .item-desc
                ling-height :.4rem
                color :#ccc
                ellipsis()
            .item-button
                margin-top :.16rem
                background :#ff9300
                padding :0 .2rem
                border-radius :.06rem
                color :#fff
                line-height :.44rem
</style>