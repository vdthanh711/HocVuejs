<template>
      <div class="ListRendering">
        <div class="Employees">
            <div v-for="employee in PMSEmployees" :key="employee.name">{{employee.name}}</div>
            <div v-for="(employee,index) in PMSEmployees" :key="employee.name">Nhân viên thứ {{(index+1)}}: {{employee.name}}</div>
        </div>
        
      </div>
      
</template>

<script>


export default {
  name: 'ListRendering',
  props: {
    msg: String
  },
  data() {
      return{
        PMSEmployees:[
          {name:'Nam'},
          {name:'Phương'},
          {name:'Đức'},
          {name:'Sang'},
          {name:'Tú'},
          {name:'Hương'},
          {name:'Thanh'},
          {name:'Thông'},
        ]
      }
     
    },
  
}
</script>

<style scoped>
  
</style>