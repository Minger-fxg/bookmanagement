<template>
  <div id="app">
    <el-container>
      <el-header id="headerBook">
        <Header/>
      </el-header>
    <el-main id="mainBook">
        <router-view></router-view>
    </el-main>
    <el-footer id="footBook">
      <Footer/>
    </el-footer >
    </el-container>
    
  </div>
</template>

<script>
 import Footer from "./components/Footer"
 import Header from "./components/Header"
 
export default {

  name: 'App',
  components: {
    Header,
    Footer,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #3d3e86;
  margin-top: 0px;
}
*{
  margin: 0;
  padding: 0;
}
#headerBook{
  background-color: #244152;
}
#mainBook{
  height: 70vh;
  /* background-color: blue; */
}
#footBook{
  height: 15px;
  /* background-color: blanchedalmond; */
}
</style>
