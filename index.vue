<template>  
  <view class="content">  
    <button @click="goToList">浏览</button>  
    <button @click="exitApp">退出</button>  
  </view>  
</template>  
  
<script>  
export default {  
  methods: {  
    goToList() {  
      uni.navigateTo({  
        url: '/pages/index/list'  
      });  
    },  
    exitApp() {  
      uni.exit(); // 注意：uni.exit()在真机调试中才有效，H5模拟器中无效  
    }  
  }  
}  
</script>  
  
<style>  
.content {  
  display: flex;  
  flex-direction: column;  
  align-items: center;  
  justify-content: center;  
  height: 100vh;  
}  
</style>
