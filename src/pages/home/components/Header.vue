<template>
<div class="header">
    <div class="header-left"><span class="iconfont ">&#xe624;</span></div>
    <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
    </div>
    <div class="header-right">
        {{city}}
        <span class="iconfont">&#xe64a;</span>
    </div>
</div>
</template>

<script>
export default {
    name: 'HomeHeader',
    props: {
        city: String
    }
}
</script>

<style scoped>
.header {
    height: .86rem;
    display: flex;
    background-color: #00b3d4;
    line-height: .86rem;
    color: #fff;
}

.header .header-left {
    width: .64rem;
    float: left;
}

.header .header-left span {
    display: block;
    text-align: center;
    font-size: .4rem;
}

.header .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
}

.header .header-right span {
    font-size: .24rem;
    margin-left: -.04rem;
}

.header .header-input {
    flex: 1;
    background: #fff;
    border-radius: .1rem;
    height: .64rem;
    margin-top: .12rem;
    margin-left: .2rem;
    color: #ccc;
    line-height: .64rem;
    padding-left: .2rem;
}
</style>
