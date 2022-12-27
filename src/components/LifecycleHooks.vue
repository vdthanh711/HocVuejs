<template>
    <div class="LifecycleHooks">
      <div>{{ message }}</div>
      <div><button @click="click1">Click</button></div>
    </div>
</template>

<script>




export default {
  name: 'LifecycleHooks',
  props: {
    msg: String
  },
  data(){
    return{
        message: 'a'
    }
  },
  method:{
    click1(){
      this.message = 'b'
      
    }
  },
  beforeCreate() {
    console.log('beforeCreate', this.property)
  },
  created() {
    console.log('Create', this.property)
  },
  beforeMount(){
    console.log('beforeMount', this.property)
  },
  mounted(){
    console.log('mounted', this.property)
  },
  beforeUpdate(){
    console.log('beforeUpdate', this.property)
  },
  Updated(){
    console.log('Updated', this.property)
  }

}
</script>

<style scoped>
  
</style>