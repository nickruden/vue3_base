<script>
  import Employee from "./components/Employee.vue"

  export default{
    components: {
      Employee
    },

    data() {
      return {
        
      }
    },

    methods: {
      // Ex. 1
      func1(name) {
        console.log(name);
      },

      // Ex. 2
      func2(name, salary) {
        console.log(name, salary);
      }
    }
  }
</script>


<template>
  <!-- Ex. 1, 2 -->
  <Employee @username="func1" @name_salary="func2"/>
</template>


<style>
 
</style>