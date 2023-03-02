<script>
export default {
  // Ex. 1
  props: {
    id: Number,
    name: String,
    surn: String,
  },

  // Ex. 1
  emits: ['changeuser'],

  data() {
    return {
      // Ex. 1
      isEdit: false,
      newName: this.name,
      newSurn: this.surn,
    }
  },
  methods: {
    // Ex. 1
    edituser() {
      this.isEdit = true;
    },
    saveuser() {
      this.isEdit = false;
      this.$emit('changeuser', this.id, this.newName, this.newSurn);
    }
  }
}
</script>

<template>
  <!-- Ex. 1 -->
  <template v-if="!isEdit">
      <h1>{{ name }}</h1>
      <h1>{{ surn }}</h1>
      <button @click="edituser">edit</button> <br>
  </template>
  <template v-else>
      <input v-model="newName">
      <input v-model="newSurn">
      <button @click="saveuser">save</button> <br>
  </template>
</template>

<style>
  body{
    margin: 0 auto;
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
  p{
    font-size: 28px;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  #main h2{
    font-size: 36px;
    margin-top: 4px;
    margin-bottom: 10px;
    text-decoration: underline;
  }
  #main ul{
    margin-top: 10px;
    text-align: left;
    margin-left: 500px;
    font-size: 24px;
  }

  input{
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

  button{
    color: rgb(26, 151, 9);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 50px;
    width: 150px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(20, 167, 45);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }

  #endword{
    font-size: 30px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
