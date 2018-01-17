<template>
    <div class="page" :id="pageId" ref="page">
        <!-- 滚动视图 -->
        <div class="wrapper">
            <!-- 展示外部接收到的dom结构 -->
            <slot></slot>
        </div>
    </div>
</template>

<script>
import IScroll from 'iscroll';

export default {
    name: 'page',
    props: {
        pageId: String
    },
    mounted(){
        //创建滚动视图
        let pageScroll = new IScroll(this.$refs.page, {})
    }
}
</script>

<style>
.page{
    width: 100%;
    position: absolute;
    top: 0; left: 0; bottom: 50px;
    overflow: hidden;
    background: #f5f5f5;
}

</style>
