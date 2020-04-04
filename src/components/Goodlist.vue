<template>
    <div>
        <ul class="goodlist">
            <li v-for="(good,index) in list" :key="index">
                <img :src="good.img" alt="">
                <p>{{good.goodname}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data(){
        var that=this;
        var url="";
        if (this.subid==1){
                url="json/computer.json";
        }else if(this.subid==2){
            url="json/phone.json";
        }
        this.$http.get(url).then(function(res){
            that.list=res.data
        });
        return{
            list:[]
        }
    },
    props:{
        subid:Number
    },
    watch:{
        subid(){
            var url="";
            var that=this;
            if (this.subid==1){
                url="json/computer.json";
            }else if(this.subid==2){
                url="json/phone.json";
            }
            this.$http.get(url).then(function(res){
                that.list = res.data;
            })
            return{
                list:[]
            }
        }
    }
}
</script>

<style scoped>
    .goodlist li{
        width:200px;
        height:200px;
        float:left;
        list-style:none;
        
    }
    .goodlist li img{
        width:180px;
        height:180px;
        
    }
    .goodlist li p{
        color:red;
        margin:0px;
    }
</style>