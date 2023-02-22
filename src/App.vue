<script>
 export default{
  name: "App",
  data() {
    return {
      // Ex. 1, 2, 3, 4, 5, 6
      arr: [1, 2, 3, 4, 5],
    }
  },
  

  methods: {
    // Ex. 1
    add: function() {
      this.arr.push(this.arr.length+1);
    },

    // Ex. 2
    delf: function() {
      this.arr.shift();
    },

    // Ex. 3
    dell: function() {
      this.arr.pop();
    },

    // Ex. 4
    delp: function() {
      this.arr.splice(this.arr.length-2, 1);
    },

    // Ex. 5
    sort: function() {
      this.arr.sort();
    },

    // Ex. 6
    rev: function() {
      this.arr.reverse();
    },
  }
}
</script>

<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1, 2, 3, 4, 5, 6 </h2>
      <ul v-for="elem in  arr">
        <li>{{ elem }}</li>
      </ul>
    </div>
    <button @click="add">add</button>

   <!-- Ex. 2 -->
    <button @click="delf">del first</button>

   <!-- Ex. 3 -->
    <button @click="dell">del last</button>

   <!-- Ex. 4 -->
    <button @click="delp">del penult</button>

   <!-- Ex. 5 -->
    <button @click="sort">sort</button>

   <!-- Ex. 6 -->
    <button @click="rev">reverse order</button>

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
  }
  #main p{
    font-size: 28px;
    margin-top: 20px;
    margin-bottom: 10px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 4px;
    text-decoration: underline;
  }
  #main .p{
    font-size: 28px;
  }
  #main ul{
    margin-top: 10px;
    text-align: left;
    margin-left: 500px;
    font-size: 24px;
  }
  #main table{
    font-size: 28px;
    border: 5px solid rgb(30, 97, 69);
    padding: 10px;
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
    height: 50px;
    width: 150px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(74, 197, 94);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }

  #endword{
    font-size: 30px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
