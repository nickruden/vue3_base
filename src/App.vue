<script>
import Employee from './components/Employee.vue'

// Ex. 1
import AddUsers from './components/AddUsers.vue'
export default {
  components: {
    Employee, 
    
    // Ex. 1
    AddUsers
  },
  data() {
    return {

      // Ex. 1
      users: [
        {
          id: 1,
          name: 'name1',
          surn: 'surn1'
        },
        {
          id: 2,
          name: 'name2',
          surn: 'surn2'
        },
        {
          id: 3,
          name: 'name3',
          surn: 'surn3'
        },
      ],
    }
  },
  methods: {

    // Ex. 1
    add(name, surn) {
      let id = this.users.length + 1;
      this.users.push({id, name, surn});
      console.log(this.users)
    }
  }
}
</script>

<template>

  <!-- Ex. 1 -->
  <AddUsers @add="add" />
</template>


<style>
 
</style>