<template>
    <div class="ConditionalRendering">
      <!-- v-if, v-else 
      v-else phải đứng ngay sau v-if hoặc v-else-if -->
      <div>{{Math.random()}}</div>
      <div v-if="(Math.random()> 0.7)">Lớn</div>
      <div v-else-if="(Math.random()< 0.3)">Nhỏ</div>
      <div v-else>Trung bình</div>
      
      
    </div>
  </template>
  
  <script>
  export default {
    name: 'ConditionalRendering',
    props: {
      msg: String
    }
  }
  </script>
  
  <style scoped>
  
  </style>
  