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
      func(apple, orange) {
        alert("Я люблю зелёные " + apple + " и оранжевые " + orange);
      }
    }
  }
</script>


<template>
  <!-- Ex. 1 -->
  <Employee @fruits="func"/>
</template>


<style>
 
</style>