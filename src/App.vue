<script>
  import Employee from "./components/Employee.vue"

  export default{
    components: {
      Employee
    },

    data() {
      return {
        // Ex. 1
        name: 'Anthony', 
        salary: '10000',
        age: '25'
      }
    }
  }
</script>


<template>
  <!-- Ex. 1 -->
  <Employee :name="name" :salary="salary" :age="age" />
</template>


<style>
 
</style>