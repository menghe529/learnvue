<template>
    <div>
        <div class="left">
            <left></left>
        </div>
        <div class="right">
            <div class="top">               
                    <img src="../../public/img/title1.png">
            </div>
            <div class="bottom">
                <div>
                    <right></right>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Left from './Left.vue'
import Right from './Right.vue'

export default {
    components:{
        Left,
        Right
    }
}
</script>

<style scoped>
    *{
        margin:0 auto;
        padding:0 auto;
    }
    .left{
        width:100px;
        height:500px;
        background-color:#f5f5f5;
        float:left;
        margin-right:10px;
    }
    .right{
        width:1000px;
        /* background-color:green; */
        height:500px;
        float:left;
    }
    .top{
        width:1000px;
        background-color:#f5f5f5;
        float:left;
    }
    .top img{
        width:100%;
        height:150px;
        /* line-height:150px; */
    }
    .bottom{
        width:1000px;
        background-color:#f5f5f5;
        float:left;
        
    }

</style>