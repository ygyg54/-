<template>  
  <view class="content">  
    <view v-for="(item, index) in listData" :key="index" class="list-item">  
      {{ item.content }} <!-- 假设API返回的每条数据包含content字段 -->  
    </view>  
    <button @click="goToForm">进入表单</button>  
  </view>  
</template>  
  
<script>  
uni.request({
    url: 'http://apis.juhe.cn/fapigw/air/provinces', // API接口地址
    method: 'GET', // 请求方法，可以是GET或POST
    dataType: 'json', // 返回数据格式
    data: {
        province: 'key', // 请求参数，根据API接口要求填写
        key: '20678ac9680f776cef9d799b1c0b86c1' // 替换为您的API密钥
    },
    header: {
        'Content-Type': 'application/x-www-form-urlencoded'
    },
    success: function (res) {
        console.log(res.data); // 打印返回的数据
    },
    fail: function (err) {
        console.log('请求失败：' + err);
    }
});
export default {  
  data() {  
    return {  
      listData: []  
    };  
  },  
  onLoad() {  
    uni.request();  
  },  
  methods: {  
    goToForm() {  
      uni.navigateTo({  
        url: '/pages/index/new1/third'  
      });  
    }  
  }  
}  
</script>  
  
<style>  
.content {  
  padding: 20px;  
}  
.list-item {  
  margin-bottom: 10px;  
}  
</style>
  
<style>  
.content {  
  padding: 20px;  
}  
.list-item {  
  margin-bottom: 10px;  
}  
</style>