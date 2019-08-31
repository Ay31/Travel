<template>
<div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" alt="">
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
                pagination: {
                    el:'.swiper-pagination',
                },
                loop: true
            },
            swiperList:[{
                id:'001',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/d52e15a5769b90dc1fc8ad15b093d70f.jpg_750x200_71f1c317.jpg'
            },
            {
                id:'002',
                imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
            }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active {
        background :#fff
    }
    .wrapper{
        background :#ccc
        overflow: hidden
        width :100%
        height :0
        padding-bottom :26.66%
    .swiper-img {
        width: 100%
    }
}
</style>