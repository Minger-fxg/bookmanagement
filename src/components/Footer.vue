<template>
    <div id="footerWrapper">
        <div id="tip1">
            <span>通讯地址：江西省南昌市湾里区</span>
        </div>
        <div id="tip2">
            <span>版权信息: &copy; 版权归属江西软件职业技术大学</span>
        </div>
    </div>
</template>

<script>
export default {
    name:"Footer",
    data(){
        return{
            message:"版权信息: &copy; 版权归属江西软件职业技术大学"
        }
    }
}
</script>
<style >
 #footerWrapper{
    text-align: center;
   }
</style>