<template>
<div>
   <div v-if="id==1">
       <Goodlist :subid="1"></Goodlist>
   </div>
   <div v-if="id==2">
       <Goodlist :subid="2"></Goodlist>
       
   </div>
   <div v-if="id==3">
       33333333
   </div>
</div>
</template>

<script>
import Msg from './Msg.js'
import Goodlist from './Goodlist.vue'
export default {
    data(){
        return{
            id:0
        }
    },
    mounted:function(){
        var that=this;
        Msg.$on('val',function(id){
            that.id = id;
        })
    },
    components:{
        Goodlist
    }
}
</script>