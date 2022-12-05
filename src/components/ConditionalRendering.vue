<template>
    <div class="ConditionalRendering">
      <!-- v-if, v-else 
      v-else phải đứng ngay sau v-if hoặc v-else-if 
      Tùy theo giá trị kiểm tra, v-if render ra với giá trị tương ứng -->
      
      <div class="login1">
        <div v-if="loginType == 'username'">
          <label >Username</label>
          <input placeholder="Enter your username">
        </div>
        <div v-else>
          <label >Email</label>
          <input placeholder="Enter your email">
        </div>
        <button @click="loginTypeButton">Login Type</button>
      </div>
      <!-- v-show: sẽ render toàn bộ ngay từ đầu, 
        tùy theo giá trị mà style là display:none  -->
      <div class="login2">
        <div v-show="loginType == 'username'">
          <label >Username</label>
          <input placeholder="Enter your username">
        </div>
        <div v-show="loginType =='Email'">
          <label >Email</label>
          <input placeholder="Enter your email">
        </div>
        <button @click="loginTypeButton">Login Type</button>
      </div>
      <!-- v-for cho object thì sẽ duyệt qua các thuộc tính 
        của object đó  và giá trị tương ứng từng thuộc tính
      nếu v-if và v-for trên 1 node, v-if sẽ được ưu tiên thực hiện-->
      
      
    </div>
  </template>
  
  <script>
  export default {
    name: 'ConditionalRendering',
    props: {
      msg: String
    },
    data() {
      return{
        loginType: 'username',
      }
    
    },
    methods: {
      loginTypeButton(){
        console.log(this.loginType)
        if(this.loginType === 'username'){
          return this.loginType = 'Email'
        }
        if(this.loginType === 'Email'){
          return this.loginType = 'username'
        }
      }
    }
  }
  </script>
  
  <style scoped>
  
  </style>
  