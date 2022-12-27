<template>
    <div class="WatchersJS">
        <div>{{ message }}</div>
        <div><button @click="changeMessage">Click me</button></div>
    </div>
</template>

<script>


export default {
  name: 'WatchersJS',
  props: {
    msg: String
  },
  data() {
    return {
      message: 'This is my first component using binding data'
    }
  },
  methods: {
    changeMessage() {
      this.message = 'this is new message'
    }
  },
  watch: {
    message(newValue, oldValue) { //khi giá trị message thay đổi, thì message ở watch sẽ thực hiện
      console.log(newValue);
      console.log(oldValue)
    }
  }
}
</script>

<style scoped>
    .WatchersJS{
      color: red;
    }
</style>