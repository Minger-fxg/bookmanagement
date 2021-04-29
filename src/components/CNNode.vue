<template>
    <div id="cnnodeWrapper">
        <div id="cnnodetitle">
            <span>论坛</span>
        </div>
        <hr>
        <div id="cnnodeContent">
        <li v-for="(value,index) in this.topicsArr" :key="index">
            <span>
                <img id="avatar" :src="value.author.avatar_url" alt="">
            </span>
            <span>
                {{value.title}}
            </span>
            
        </li>
    </div>
    </div>
    
</template>

<script>
import Axios from 'axios'
export default {
    Axios,
    data(){
        return{
            topicsArr:[]
        }
    },
    beforeCreate(){
        // console.log("this vue before")
    },
    created(){
        let that = this 
        // console.log("this vue is runing")
        Axios.get('https://cnodejs.org/api/v1/topics').then(function(reponse){
            // console.log(reponse.data)
            if(reponse.data.success){
                that.topicsArr=reponse.data.data;
            }

        })
    }
}
</script>

<style >
    #avatar{
        width: 20px;
        height: 20px;
        
    }
</style>