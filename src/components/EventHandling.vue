<template>
    <!-- Lắng nghe sự kiện 
    Dùng v-on:tên-sự-kiện, viết tắt là @tên-sự-kiện-->
    <div class="example-1">
        <div >
            <input v-model="task" type="text" placeholder="Your task" class="form-control">
            <button @click="addTask" >Submit</button>
            <div v-for="(task, index) in tasks" :key="index">{{task.name}}</div>
        </div> 
    </div>
    <!-- Event modifier hậu tố 
    event.stop tương đương event.stopPropagation() sự kiện sẽ không lan truyền
    event.prevent tương đương event.preventDefault() sự kiện không reload lại trang
    -->
</template>

<script>


export default {
  name: 'EventHandling',
  props: {
    msg: String
  },
  data(){
    return {
        task: '',
        tasks:[]
    }
  },
  methods:{
    addTask(){
     if(this.task.length ===0) return;
     this.tasks.push({
        name: this.task
     })
    }
  }
}
</script>

<style scoped>
  
</style>