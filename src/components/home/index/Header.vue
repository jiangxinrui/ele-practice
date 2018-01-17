<template>
<div class="header">
    <div class="position">
        <img src="../../../../static/images/position.png" alt="">
        福中三路深圳市民中心
    </div>

    <div class="search">
        <a href="">
            <img src="../../../../static/images/search.png" alt="">&nbsp;
            <span>搜索商家、商品名称</span>
        </a>
        
    </div>
</div>
</template>

<script>
export default {
    name: 'home-header'
}
</script>

<style scoped>
.header{
    width: 100%;
    height: 96px;
    background-image: linear-gradient(90deg,#0af,#0085ff);
    display: flex;
    flex-direction: column;
    /* align-items: center; */
}
.position{
    box-sizing: border-box;
    padding: 16px 16px 0 16px;
    font-size: 18px;
    color: white;
    display: flex;
    height: 50%;
}
.position img{
    width: 18px;
    height: 20px;
}

.search{
    width: 100%;
    height: 50%;
    box-sizing: border-box;
    padding: 8px 10px;
}
.search a{
    width: 100%;
    height: 100%;
    background: white;
    display: inline-block;
    display: flex;
    align-items: center;
    justify-content: center;
}
.search a img{
    width: 14px;
    height: 14px;
    display: inline-block;
}
.search a span{
    color: #ccc;
    font-size: 14px;
}
</style>
