<template>
<div>
    <div class="recommend-title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <img class="item-img" :src="item.imgUrl" alt="">
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
    data: function () {
        return {
            recommendList: [{
                id: '0001',
                imgUrl: '//img1.qunarzz.com/sight/p0/1508/96/b195d4ecbd48b7fc3ae049106f15c7ef.water.jpg_256x160_92934f01.jpg',
                title: '山东泰山',
                desc: '会当凌绝顶，一览纵山小。泰山风景以壮丽著称。重叠的山势，厚重的形体，苍松巨石的烘托，云烟的变化，使它在雄浑中兼有明丽，静穆中透着神奇。'
            }, {
                id: '0002',
                imgUrl: '//img1.qunarzz.com/sight/p0/1412/46/45386387700af94fd228995c9999eb14.water.jpg_256x160_23e17822.jpg',
                title: '蓬莱阁',
                desc: '道教传说中著名的神仙住所和人间仙境'
            }, {
                id: '0003',
                imgUrl: '//img1.qunarzz.com/sight/p0/1707/a3/a3924161475dee37a3.img.jpg_256x160_9163f4e5.jpg',
                title: '青岛海昌极地海洋公园',
                desc: '一起与极地动物们亲密接触吧'
            }]
        }
    }
}
</script>

<style scoped>
.recommend-title {
    margin-top: .2rem;
    line-height: .8rem;
    background: #eee;
    text-indent: .2rem;
}

.item {
    overflow: hidden;
    height: 1.9rem;
    display: flex;
}

.item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: .1rem;
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

.item-button {
    line-height: .44rem;
    background: #ff9300;
    padding: 0 .2rem;
    border-radius: .06rem;
    color: #eee;
    margin-top: .16rem;
}
</style>
