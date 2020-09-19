<template>
<div class="list" ref="wrapper">
    <div>
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="botton-list">
                <div class="button-wrapper">
                    <div class="button">北京</div>
                </div>
            </div>

        </div>
        <div class="area">
            <div class="title border-topbottom">热门城市</div>
            <div class="botton-list">
                <div class="button-wrapper" v-for="item of hot" :key="item.id">
                    <div class="button">{{item.name}}</div>
                </div>

            </div>
        </div>

        <div class="area" v-for="(item,key)  of  cities" :key="key">
            <div class="title border-topbottom">{{key}}</div>
            <div class="item-list" v-for="innerItem of item" :key="innerItem.id">
                <div class="item border-bottom">{{innerItem.name}}</div>
            </div>
        </div>

    </div>
</div>
</template>

<script>
import Bscroll from 'better-scroll'

export default {
    name: 'CityList',
    props: ['hot', 'cities'],
    computed: {
        a: function () {
            return this.cities.A !== undefined
        }
    },
    mounted: function () {
        this.scroll = new Bscroll(this.$refs.wrapper)
    }
}
</script>

<style scoped>
.title {
    line-height: .54rem;
    background: #eee;
    padding-left: .2rem;
    color: #666;
    font-size: .26rem;
}

.border-topbottom::after,
.border-topbottom::before {
    border-color: #ccc;

}

.botton-list {
    padding: .1rem .1rem;
    overflow: hidden;
    padding: .1rem .6rem .1rem .1rem;
}

.button-wrapper {
    width: 33.33%;
    float: left;
}

.button {
    text-align: center;
    margin: .1rem .1rem;
    border: .02rem solid #ccc;
    padding: .1rem 0;
    border-radius: .06rem;
}

.item {
    line-height: .76rem;
    padding-left: .2rem;
}

.border-bottom::after,
.border-bottom::before {
    border-color: #ccc;

}

.list {
    overflow: hidden;
    position: absolute;
    top: 1.58rem;
    left: 0;
    right: 0;
    bottom: 0;
}

.list>div {
    height: 740rem;
}
</style>
