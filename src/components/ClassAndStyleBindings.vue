<template>
    <div class="ClassAndStyleBindings">
       <!-- Class binding -->
      <div class="binding-html">
        <!-- v-bind:class có thể truyền một đối tượng vào v-bind:class 
          và tùy thuộc vào giá trị từng thuộc tính của đối tượng 
          mà các class khác nhau được gán vào
          -->
        <div class="text-title" :class="{active: isActive, hide: isHide, bold: isBold, show: isShow}">
            This is text
        </div>
        <!-- truyền 1 array vào v-bind:class -->
        <div class="text-title" :class="[activeClass, boldClass]">
            This is text
        </div>
        <!-- truyền 1 object vào v-bind:class -->
        <div class="text-title" :class="classObject">
            This is text
        </div>
        <div>
          <!--v-on dùng để lắng nghe các sự kiện trên DOM -->
            <button @click="isActive = true">Change color red</button>
        </div>
        <div>
            <button @click="(isHide = true, isShow = false)">Hide text</button>
        </div>
        <div>
            <button @click="isBold = true">Bold text</button>
        </div>
        <div>
            <button @click="(isShow = true, isHide = false)">Show text</button>
        </div>
      </div>
      <!-- Style binding -->
      <div class="text-title" :class="classObject" :style="{backgroundColor: color}">
        This is text
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ClassAndStyleBindings',
    props: {
      msg: String
    },
    data(){
        return {
            isActive: false,
            isHide: false,
            isBold: false,
            isShow: false,
            activeClass: 'active',
            boldClass: 'bold',
            classObject: {
                active: true,
                bold: true
            },
            color: 'yellow'
        }
        
    }
  }
  </script>
  
  <style scoped>
    .active{
      color: red;
    }
    .hide{
      display: none;
    }
    .bold{
      font-weight: bold;
    }
    .show{
      display: block;
    }
  </style>
  