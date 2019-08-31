<template>
    <div class="icons">
    <swiper >
        <swiper-slide v-for="(page,index) of pages" :key='index'>
            <div class="icon" v-for="icon of page" :key='icon.id'>
                <div class="icon-img">
                    <img class="icon-img-content" :src='icon.iconSrc'>
                 </div>
                    <p class="icon-desc">{{icon.iconDesc}}</p>
        </div>
        </swiper-slide>

  </swiper>



    </div>
</template>

<script>
export default {
    name:'HomeIcons',
    data () {
        return {
            iconList :[{
                id:'001',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                iconDesc:'景点门票'
            },
            {
                id:'002',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                iconDesc:'东莞必游'
            },
            {
                id:'003',
                iconSrc:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/f44e55751b9343cfb624e2982261f485.png',
                iconDesc:'黄腾峡景区'
            },
            {
                id:'004',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1805/3a/754b47f658e9c602.png',
                iconDesc:'消暑玩水'
            },
            {
                id:'005',
                iconSrc:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/184e261814a5d07a5d3d08cd29cf590d.png',
                iconDesc:'长隆度假区'
            },
            {
                id:'006',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1803/87/20656da0ac042002.png',
                iconDesc:'洞天仙境'
            },
            {
                id:'007',
                iconSrc:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cba147cf6cfcea7109d0bff6aac6f626.png',
                iconDesc:'香市动物园'
            },
            {
                id:'008',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1803/90/59a2f523ee2f9202.png',
                iconDesc:'隐贤山庄'
            },
            {
                id:'009',
                iconSrc:'http://img1.qunarzz.com/piao/fusion/1803/17/99402a22ce4af302.png',
                iconDesc:'肇庆星湖'
            },
            {
                id:'010',
                iconSrc:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/bda58ffc3016edad84e656e8a94b0321.png',
                iconDesc:'广州融创'
            }
            ]
        }
    },
    computed:{
        pages () {
            const pages = []
            this.iconList.forEach((item,index)=>{
                const page = Math.floor(index/8)
                if(!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages;
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    @import '~styles/varibles.styl'

    .icons
        overflow hidden
        height 0
        padding-bottom 50%
        .icon
            overflow hidden
            position relative
            width 25%
            height 0
            padding-bottom 25%
            float left
            background #fff
            .icon-img
                position absolute
                top 0
                left 0
                right 0
                bottom .28rem
                padding .1rem
                box-sizing border-box
                background #fff
                .icon-img-content
                    margin 0 auto
                    display block
                    height 100%
            .icon-desc
                position absolute
                left 0
                right 0
                bottom 0
                height .45rem
                line-height .45rem
                text-align center
                color $darkTextColor
                ellipsis()
                font-size .25rem
               
</style>