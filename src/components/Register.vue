<template>
  <div id="registerWrapper">
    <div id="registerContent">
        <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>用户注册</span>
      </div>
      <div id="registerContmentbody">
          <el-input id="newUsername" v-model="newUser.newUsername" class="inputWrapper" clearable></el-input>
          <el-input id="newPassword" v-model="newUser.newPassword" class="inputWrapper" show-password clearable></el-input>
          
      </div>
      <div id="registerConrmentSubmit">
          <el-button id="systemSubmit" @click="registerSystem">注册</el-button>
      </div>
    </el-card>
    </div>
  </div>
</template>

<script>
import Axios from 'axios'
export default {
  
  name: "register",
  data() {
    return {
      newUser:{
          newUsername:"",
          newPassword:""
      }
    };
  },
  methods:{
    registerSystem(){
      Axios.post('http://localhost:3000/register',{
        params:this.newUser
      }).then(function(response){
        alert(response.data)
      })
    }
  }
};
</script>
<style>
#registerWrapper {
  height: 100%;
  /* background-color: bisque; */
}
#registerContent{
    margin: 0 auto;
    padding-top: 100px;
    width: 400px;
    
}
.inputWrapper{
    margin-top: 20px;
}
#registerConrmentSubmit{
    text-align: center;
}
#systemSubmit{
  margin-top: 20px;
    background-color: #0a9588;
    color: aliceblue;
}
</style>