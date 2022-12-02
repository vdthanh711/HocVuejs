<template>
    <div class="TemplateSyntax">
      <!-- Text -->
        <!--{{}}Trả về theo giá trị biến nắm bên trong  -->
        <div>Xin chao {{message}}</div> 
        <!-- v-once lưu giá trị đầu tiên nhận vào và không thay đổi-->
        <div v-once>Xin chao {{message}}</div>
        <button @click="click">aaa</button>
      <!-- rawHtml xuất ra html thuần túy -->
        <div v-html="rawHtml" ></div>
      <!-- Thuộc tính sử dụng v-bind -->
    </div>
   
  </template>
  
  <script>


  export default {
    name: 'TemplateSyntax',
    props: {
      msg: String
    },
    data(){
        return{
            message: 'Thanh',
            rawHtml: '<h1>HELLO '+'<span style="color:blue;">'+'WORLD</span>'+'</h1>',
            
        }
    },
    methods: {
      click(){
        this.message= 'Sang'
      }
    }
   
  }
  </script>
  
  <style scoped>
    
  </style>
  