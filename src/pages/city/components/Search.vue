<template>
<div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音">
</div>
</template>

<script>
export default {
    name: 'CitySearch'
}
</script>

<style scoped>
.search {
    height: .72rem;
    background: #00b3d4;
    padding: 0 .1rem;
}

.search-input {
    height: .62rem;
    width: 100%;
    line-height: .62rem;
    text-align: center;
    border-radius: .06rem;
    color: #666;
    padding: 0 .1rem;
    box-sizing: border-box;
}
</style>
