<template>
    <div id="headerWrapper">
        <div id="headerTitle">
            <span>{{message}}</span>
        </div>
        <div id="headerFunction">
            <router-link to="/Login">
                <el-button>系统登录</el-button>
            </router-link>
            <router-link to="/Work">
                <el-button>工作中心</el-button>
            </router-link>
             <router-link to="/Reader">
                <el-button>读者信息</el-button>
            </router-link>
               <router-link to="/Book">
                <el-button>图书信息</el-button>
            </router-link>
               <router-link to="/cnnode">
                <el-button>node论坛</el-button>
            </router-link>
            
            
            
            
        </div>
    </div>
</template>

<script>
export default {
    name:"HeaderBook",
    data(){
        return{
            message:"江西软件职业技术大学-新型图书管理系统"
        }
    }
}
</script>
<style>
    #headerTitle{
        float: left;
        display: inline-block;
        height: 60px;
        line-height: 60px;
        color: aliceblue;
        font-size: 24px;
        font-weight: bolder;
    }
    #headerFunction{
        float: right;
        display: inline-block;
        margin-top:10px;
    }
    #headerFunction>*>*{
        background-color: #0a9588;
        color: aliceblue;
        border: #0a9588;
        margin-right: 10px;
    }
</style>