<template>

      <div class="ListRendering">
        <!-- v-for cho object thì sẽ duyệt qua các thuộc tính 
        của object đó  và giá trị tương ứng từng thuộc tính
      nếu v-if và v-for trên 1 node, v-if sẽ được ưu tiên thực hiện-->
        <div class="v-for">
           
            <div v-for="(employee,index) in PMSEmployees" :key="employee.name">Nhân viên thứ {{(index+1)}}: {{employee.name}}</div>
        </div>
        <!--Hiển thị kết quả đã được lọc hoặc sắp xếp  -->
            <div v-for="employee1 in newEmployees" :key="employee1.name">{{employee1.name}}</div>
        <!-- v-for với 1 dãy -->
        <div>
          <span v-for="n in 10" :key="n">{{ n }} </span>
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
        ],
        
      }
     
    },
  // methods: {
  //   firstLetter:function(){
  //     return this.PMSEmployees.filter(function(employee1){
  //       return employee1.name.[0] === 'T'
        
  //     })
  //   },
    
  // }
  computed: {
    newEmployees() {
      return this.PMSEmployees.filter(employe => employe.name.charAt(0) === 'T')
    }
  }
}
</script>

<style scoped>
  
</style>