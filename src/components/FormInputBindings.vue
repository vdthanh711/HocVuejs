<template>
  <!-- v-model luôn coi data là nguồn đáng tin cậy nhất-->
  <div id="FormInputBindings">
    <div class="example">
      <input v-model="message" placeholder="Nhập thông điệp">
      <p>Thông điệp: {{ message }}</p>
    </div>
    <div id='example-3'>
  <input type="checkbox" id="Java" value="java" v-model="checkedNames">
  <label for="Java">Java</label><br>
  <input type="checkbox" id="#C" value="#c" v-model="checkedNames">
  <label for="#C">#C</label><br>
  <input type="checkbox" id="JavaScript" value="javascript" v-model="checkedNames">
  <label for="JavaScript">JavaScript</label>
  <br>
  <span>Các mục đã chọn: {{ checkNamesTransform }}</span>
</div>
  </div>
</template>

<script>


export default {
  name: 'FormInputBindings',
  props: {
    msg: String
  },
  data(){
    return{
      message: '',
      checkedNames: []
    }
  },
  computed: {
    checkNamesTransform() {
      return this.checkedNames.map(value => {
        const firstChar = value.charAt(0)
        return firstChar.toUpperCase() + value.slice(1)
      })
    }
  }
}
</script>

<style scoped>
  
</style>