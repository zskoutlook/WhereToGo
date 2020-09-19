<template>
<div class="header">
    城市选择
    <router-link to="/">
        <div>
            <span class="iconfont header-bcak">&#xe624;</span>
        </div>
    </router-link>

</div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header {
    overflow: hidden;
    height: .86rem;
    line-height: .86rem;
    text-align: center;
    color: #fff;
    background-color: #00b3d4;
    font-size: .32rem;
    position: relative;
}

.header div {
    height: .86rem;
    width: .86rem;
    position: absolute;
    top: 0;
    left: 0;

}

.header-bcak {
    width: .64rem;
    text-align: center;
    font-size: .4rem;
    color: #fff;
}
</style>
