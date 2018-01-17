<template>
    <nav class="tabnav one-top-px">
        <router-link class="tab" v-for="(tabitem, index) in tabData" 
        :key="index" :to="tabitem.path">
            {{tabitem.title}}
        </router-link>
    </nav>
</template>

<script>
export default {
    name: 'navs',
    data(){
        return {
            tabData: [
                {title: '首页', path: '/home'},
                {title: '发现', path: '/discover'},
                {title: '订单', path: '/order'},
                {title: '我的', path: '/mine'}
            ]
        }
    }
}
</script>

<style scoped>
.tabnav{
    position: absolute;
    left: 0; bottom: 0;
    width: 100%;
    height: 49px;
    background: white;
    border-top: 1px solid #ccc;
    display: flex;
}
.tab{
    flex: 1;
    text-align: center;
    line-height: 49px;
    color: black;
    font-size: 16px;
    text-decoration: none;  /* 去掉下划线 */
}
/* 设置tab切换de样式 */
.tabnav .router-link-active{
    color: #008eff;
    font-weight: 900;
}
</style>
