<script>
  import Employee from "./components/Employee.vue"

  export default{
    components: {
      Employee
    }
  }
</script>


<template>
  <!-- Ex. 1 -->
  <Employee :arr="['a', 'b', 'c', 'd', 'e']" />
</template>


<style>
 
</style>