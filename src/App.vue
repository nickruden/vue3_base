<script>
 export default{
  name: "App",
  data() {
    return {
      // Ex. 1
      users: [
			  {
				  id: 1,
				  name: 'name1',
				  salary: 100,
				  age: 30,
          isEdit: false,
			  },
			  {
				  id: 2,
				  name: 'name2',
				  salary: 200,
				  age: 40,
          isEdit: false,
			  },
			  {
				  id: 3,
				  name: 'name3',
				  salary: 300,
				  age: 50,
          isEdit: false,
			  },
		  ],
    }
  },

  methods: {
    // Ex. 1
    deluser: function(id) {
      this.users = this.users.filter((user) => { return user.id !== id; } );
    },

    edituser(user) {
      user.isEdit = true;
    },

    saveuser(user) {
      user.isEdit = false;
    }
  }
}
</script>

<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1</h2>
      <table>
        <thead>
          <tr>
            <td>Name</td>
            <td>Salary</td>
            <td>Age</td>
            <td>Delete</td>
            <td>Edit</td>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(user, index) in users" :key="user.id">
            <template v-if="!user.isEdit">
              <td>{{ user.name }}</td>
              <td>{{ user.salary }}</td>
              <td>{{ user.age }}</td>
              <td><a href="#" @click="deluser(user.id)">del</a></td>
              <td><a href="#" @click="edituser(user)">edit</a></td>
            </template>

            <template v-if="user.isEdit">
              <td><input v-model="user.name"></td>
              <td><input v-model="user.salary"></td>
              <td><input v-model="user.age"></td>
              <td><a href="#" @click="saveuser(user)">save</a></td>
            </template>
          </tr>
        </tbody>
      </table>
    </div>

    <p id="endword">by NikitaRudenko</p>
  </div>
</template>

<style>
  #main{
    margin-top: 50px;
    margin-bottom: 50px;
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1100px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:60px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  #main div{
    margin-top: 10px;
    margin-bottom: 40px;
  }
  #main p{
    font-size: 24px;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  #main h2{
    font-size: 36px;
    margin-top: 4px;
    margin-bottom: 10px;
    text-decoration: underline;
  }
  #main .p{
    font-size: 24px;
  }
  #main .pinput{
    text-transform: uppercase;
  }
  #main ul{
    margin-top: 10px;
    text-align: left;
    margin-left: 500px;
    font-size: 24px;
  }
  #main li{
    cursor: pointer;
  }
  #main table{
    margin: 0 auto;
    margin-top: 20px;
    font-size: 28px;
    border: 5px solid rgb(30, 97, 69);
    padding: 10px;
  }
  #main td{
  padding: 10px;
  margin: 10px;
  border-radius: 3px;
  }
  #main a{
    font-size: 24px;
    color: rgb(189, 255, 177);
  }
  #main a:hover{
    font-size: 24px;
    color: rgb(22, 88, 69);
  }

  #main button{
    margin-top: 20px;
    margin-right: 20px;
    color: rgb(26, 151, 9);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 70px;
    width: 170px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(20, 167, 45);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  
  #main input{
    font-size: 20px;
    max-width: 500px;
    height: 40px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    text-align: center;
    margin-right: 10px;
  }
  #main .inptext{
    margin-top: 10px;
    font-size: 20px;
    width: 400px;
    height: 40px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    text-align: center;
    margin-right: 10px;
  }
  #main .inpfio{
    margin-top: 10px;
    font-size: 20px;
    width: 400px;
    height: 40px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    text-align: center;
    margin-right: 10px;
  }

  #main textarea{
    margin-bottom: -10px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    padding: 10px;
    margin-right: 10px;
  }

  #main .checkboxs{
    font-size: 20px;
  }

  #main select{
    margin-top: 10px;
    margin-bottom: 5px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    padding: 10px;
    margin-right: 10px;
  }
  #main select:hover{
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(38, 116, 64, 0.616);
    color: rgb(131, 255, 214);
  }

  #endword{
    font-size: 30px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
