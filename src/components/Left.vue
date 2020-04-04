<template>
    <div>
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li @click="menu1">笔记本 </li>
            <li @click="menu2">手机</li>
            <li @click="menu3">零食</li>
            <li>家庭用品</li>
            <li>家电</li>
            <li>化妆</li>
            <li>衣物</li>
        </ul>
    </div>
</template>
<script>
import Msg from './Msg.js'
export default {
    methods:{
        menu1:function(){
            Msg.$emit('val', '1')
        },
        menu2:function(){
            Msg.$emit('val', '2')
        },
        menu3:function(){
            Msg.$emit('val', '3')
        }
    }
}
</script>
<style scoped>
    .title{
        width:100px;
        color:red;
    }
    .menu{
        padding:0;
        margin:0px;
    }
    .menu li{
        list-style:none;
        width:100px;
        height:50px;
        line-height:50px;
        background-color:white;
        text-align: center;
        cursor:pointer;
        margin-bottom:2px;
        /* padding-left:0px 0px; */
    }
</style>