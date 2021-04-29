<template>
  <div id="loginWrapper">
    <div id="loginContent">
        <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>系统登录</span>
        <el-button style="float: right; padding: 3px 0" type="text">
           忘记密码
        </el-button>
      </div>
      <div id="loginContmentbody">
          <el-input id="username" v-model="user.usename" class="inputWrapper" clearable></el-input>
          <el-input id="password" v-model="user.password" class="inputWrapper" show-password clearable></el-input>
          
      </div>
      <div>
        <router-link to="/Register">
          <el-button style="float: right; padding: 3px 0；margin-top:100px" type="text">
           用户注册
          </el-button>
        </router-link>
      </div>
      <div id="loginConrmentSubmit"> 
        <el-button id="systemSubmit" @click="loginSystem">登录</el-button>
      </div>
    </el-card>
    </div>
  </div>
</template>

<script>
import Axios from 'axios'
export default {
  
  name: "Login",
  data() {
    return {
      user:{
          username:"",
          password:""
      }
    };
  },
  methods:{
    loginSystem(){
      Axios.get('http://localhost:3000/Login').then(function(response){
        alert(response.data)
      })
    }
  }
};
</script>
<style>
#loginWrapper {
  height: 100%;
  /* background-color: bisque; */
}
#loginContent{
    margin: 0 auto;
    padding-top: 100px;
    width: 400px;
    
}
.inputWrapper{
    margin-top: 20px;
}
#loginConrmentSubmit{
    text-align: center;
}
#systemSubmit{
  margin-top: 20px;
    background-color: #0a9588;
    color: aliceblue;
}
</style>