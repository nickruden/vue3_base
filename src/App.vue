<script>
import Employee from './components/Employee.vue'
export default {
  components: {
    Employee
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
    change(id, name, surn){
      this.users = this.users.map((user) => {
        if(user.id === id){
          user.name = name;
          user.surn = surn;
        }
        return user;
      });
    }
  }
}
</script>

<template>
    <!-- Ex. 1 -->
  <Employee v-for="user in users"
		:id="user.id"
		:name="user.name"
		:surn="user.surn"
		:key="user.id"

    @changeuser="change" />
</template>


<style>
 
</style>