<template>
    <div class="ComputedProperties">
      <!-- Khi gọi computed không được thêm dấu (), 
        computed không nhận được tham số đầu vào. -->
        <div>{{ reverseMessage }}</div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ComputedProperties',
    props: {
      msg: String
    },
    data() {
      return {
        message: 'một con mèo'
      }
    },
      computed: {
        reverseMessage() {
          return this.message.split(' ').reverse().join(' ')
      }
    }
  }
  </script>
  
  <style scoped>
  
  </style>
  