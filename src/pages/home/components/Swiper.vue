<template>
<div class="wrapper">
    <swiper :options="swiperOptions" v-if="showSwiper">
        <swiper-slide v-for="item of list" :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" />
        </swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
</div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    props: {
        list: Array
    },
    data: function () {
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            }
        }
    },
    computed: {
        showSwiper: function () {
            return this.list.length
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
