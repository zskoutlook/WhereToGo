<template>
<div class="icons">
    <swiper :options="swiperOptions">
        <swiper-slide v-for="(page,index) of pages" :key="index">
            <div class="icon" v-for="item of page" :key="item.id">
                <div class="icon-img">
                    <img class="icon-img-content" :src="item.imgUrl" alt="">
                </div>
                <p>{{item.desc}}</p>
            </div>
        </swiper-slide>
    </swiper>

</div>
</template>

<script>
export default {
    props: {
        list: Array
    },
    name: 'HomeIcons',
    data: function () {
        return {
            swiperOptions: {
                autoplay: false
            }
        }
    },
    computed: {
        pages: function () {
            const pages = []
            this.list.forEach((item, index) => {
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

<style scoped>
.icons {
    margin-top: .1rem;
}

.icons>>>.swiper-container {
    height: 0;
    padding-bottom: 50%;
}

.icon {
    width: 25%;
    float: left;
    padding-bottom: 25%;

    height: 0;
    position: relative;
}

.icon-img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: .44rem;
    box-sizing: border-box;
    padding-bottom: 0.1rem;
}

.icon-img-content {
    display: block;
    margin: 0 auto;
    height: 100%;
}

p {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 0.44rem;
    line-height: 0.44rem;
    color: #333;
    text-align: center;
    font-size: .3rem;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
</style>
