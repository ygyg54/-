<template>  
  <view class="content">  
    <input type="text" placeholder="姓名" v-model="formData.name" />  
    <input type="text" placeholder="建议" v-model="formData.suggestion" />  
	
    <input type="text" placeholder="验证码" v-model="formData.captcha" />  
    <button @click="submitForm">提交</button>  
  </view>  
</template>  
  
<script>  
export default {  
  data() {  
    return {  
      formData: {  
        name: '',  
        suggestion: '',  
        captcha: ''  
      }  
    };  
  },  
  methods: {  
    submitForm() {  
      uni.showToast({  
        title: '提交成功',  
        icon: 'success'  
      });  
      // 这里可以添加将表单数据发送到服务器的逻辑  
    }  
  }  
}  
</script>  
  
<style>  
.content {  
  padding: 20px;  
}  
input {  
  margin-bottom: 10px;  
}  
</style>
