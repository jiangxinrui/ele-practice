<template>
<div class="banner">
    <!--  轮播结构  -->
    <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide one">
                <a class="a-goods" href="#" v-for="(item, index) in datalist">{{item.name}}</a>
            </div>

            <!-- 第二页 -->
            <div class="swiper-slide two">
                <a href="#"></a>
            </div>
        </div>

        <!--底部导航条-->
        <div class="swiper-pagination"></div>
    </div>

</div>
</template>

<script>
import Swiper from '../../../../static/js/swiper.js';
import axios from 'axios'

export default {
    name: 'home-banner',
    data(){
        return {
            datalist: []
        }
    },
    mounted(){
        //创建轮播结构
        var swiper = new Swiper('.swiper-container',{
            pagination : '.swiper-pagination',
            autoplay : 9000
        });
        
        axios.get('/restapi/shopping/openapi/entries?latitude=22.54286&longitude=114.059563&templates[]=main_template&templates[]=favourable_template&templates[]=svip_template')
        .then((data)=>{
            console.log('请求成功了');
            var that = this; //
            data.data[0].entries.map(function(item){
                that.datalist.push(item);
                //console.log(that.datalist);
            })
           
        })
    }
}
</script>

<style scoped>
.banner{
    width: 100%;
    height: 280px;
    background: lightgoldenrodyellow;
    margin-bottom: 12px;
}
/*Swiper 轮播图*/
.swiper-container {
    width: 100% !important;
    height: 180px;
}
.one{
    background: goldenrod;
}
.two{
    background: hotpink;
}
.a-goods{
    display: inline-block;
    width: 25%;
    height: 50px;
    line-height: 50px;
    text-align: center;
}
</style>