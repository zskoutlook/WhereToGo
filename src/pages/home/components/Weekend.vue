<template>
<div>
    <div class="title">周末去哪</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
                <img class="item-img" :src="item.imgUrl" alt="">
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
    data: function () {
        return {
            recommendList: [{
                id: '0001',
                imgUrl: '//imgs.qunarzz.com/p/p19/1809/b9/2a3d362aabcbb02.jpg_256x160_28907832.jpg',
                title: '重庆',
                desc: '会当凌绝顶，一览纵山小。泰山风景以壮丽著称。重叠的山势，厚重的形体，苍松巨石的烘托，云烟的变化，使它在雄浑中兼有明丽，静穆中透着神奇。'
            }, {
                id: '0002',
                imgUrl: '//imgs.qunarzz.com/p/p97/1512/73/97da2a9e39df59f7.jpg_256x160_acb41adf.jpg',
                title: '成都',
                desc: '道教传说中著名的神仙住所和人间仙境'
            }, {
                id: '0003',
                imgUrl: '//imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg',
                title: '丽江',
                desc: '一起与极地动物们亲密接触吧'
            }]
        }
    }
}
</script>

<style scoped>
.title {
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
}

.item-img-wrapper {
    height: 0;
    overflow: hidden;
    padding-bottom: 33.9%;
}

.item-img {
    width: 100%;

}

.item-info {
    flex: 1;
    min-width: 0;
    padding: .1rem;
}

.item-title {
    line-height: .54rem;
    font-size: .32rem;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.item-desc {
    line-height: .4rem;
    color: #ccc;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
</style>
