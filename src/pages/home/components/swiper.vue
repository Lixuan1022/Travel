<template>
    <div class="wrapper">
     <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    


    <div class="swiper-pagination"  slot="pagination"></div>

  </swiper>
  </div>
</template>

<script>
export default {
    name:'HomeSwiper',
    data(){
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: '0001',
                imgUrl:"https://dimg04.c-ctrip.com/images/zg0l170000012z984F719.jpg"
            },{
                id: '0002',
                imgUrl:"https://dimg04.c-ctrip.com/images/zg0l1800000154a4jA30A.jpg"
            }]
        }
    }
}
</script>

<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active{
    background: #fff
}
.wrapper{
    width 100%
    height 0
    overflow hidden
    padding-bottom 31.25%
}
    .swiper-img{
        width 100%
    }
</style>