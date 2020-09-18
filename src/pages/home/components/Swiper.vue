<template>
<div class="wrapper">
    <swiper :options="swiperOptions">
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
</div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data: function () {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                    id: '0001',
                    imgUrl: 'http://imgs.qunarzz.com/vs_ceph_vcimg/1cfbdaa2682ada2f854ea6114b3677c8.jpeg'
                },
                {
                    id: '0002',
                    imgUrl: 'http://imgs.qunarzz.com/vs_ceph_vcimg/7176acd77332a433af9636eb9a2c338c.jpeg'
                },
                {
                    id: '0003',
                    imgUrl: '//imgs.qunarzz.com/vs_ceph_vcimg/7176acd77332a433af9636eb9a2c338c.jpeg'
                }
            ]
        }
    }
}
</script>

<style scoped>
.wrapper>>>.swiper-pagination-bullet-active {
    background: #fff;
}

.wrapper {
    width: 100%;
    height: 0;
    padding-bottom: 30%;
    overflow: hidden;
    background-color: #eee;

}

.swiper-img {
    width: 100%;
}
</style>
