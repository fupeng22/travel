<template>
    <div>
       
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" 
        src="http://img1.qunarzz.com/sight/p0/2005/23/23c1b2b13230b966a3.water.jpg_600x330_5cccec1e.jpg"/>
        <div class="banner-info">
            <div class='banner-title'>
                上海迪士尼乐园
            </div>
            <div class="banner-number"> 
                <span class="iconfont banner-icon">&#xe692;</span>
            </div>
        </div>
    </div>

     <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
    </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name:'DetailBanner',
    components:{
        CommonGallary
    },
    data(){
        return{
            imgs:['http://img1.qunarzz.com/sight/p0/2005/23/23c1b2b13230b966a3.water.jpg_r_800x800_51ae7c16.jpg'
            ,'http://img1.qunarzz.com/sight/p0/2005/c4/c47eda0a56b427f9a3.water.jpg_r_800x800_7c925806.jpg'
            ,'http://img1.qunarzz.com/sight/p0/2005/95/9595b69378a15cf5a3.water.jpg_r_800x800_4243bcf8.jpg'],
            showGallary:false
        }
       
    },
    methods:{
        handleBannerClick:function(){
            this.showGallary=true
        },
        handleGallaryClose:function(){
            this.showGallary=false;
        }
    }
}
</script>
<style lang='stylus' scoped>
    .banner
        position :relative
        overflow :hidden
        height:0
        padding-bottom:55%
        .banner-img
            width:100%
        .banner-info
            background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
            display :flex
            position:absolute
            left:0
            right:0
            bottom:0
            line-height: .6rem
            color:#fff
            .banner-title
                flex:1
                font-size :.32rem
                padding :0 .2rem
            .banner-number
                height: .32rem
                line-height: .32rem
                margin-top: .14rem
                padding: 0 .4rem
                border-radius: .2rem
                background: rgba(0, 0, 0, .8)
                font-size: .24rem
                .banner-icon
                    font-size: .24rem
                
</style>