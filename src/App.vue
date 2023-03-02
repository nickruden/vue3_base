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
      func1() {
        alert("Упражнение №1. Функция 1");
      },

      func2() {
        alert("Упражнение №1. Функция 2");
      }
    }
  }
</script>


<template>
  <!-- Ex. 1 -->
  <Employee @show1="func1" @show2="func2"/>
</template>


<style>
 
</style>