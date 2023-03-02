<script>
 export default{
  name: "Employee",
  props: [],

  // Ex. 1
  emits: ['fruits'],

  data() {
    return {

    }
  },

  methods: {

  }
}
</script>


<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1</h2>
      <button @click="$emit('fruits', 'яблоки', 'апельсины')">Передать данные</button>
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
  #main ul{
    margin-top: 10px;
    text-align: left;
    margin-left: 500px;
    font-size: 24px;
  }

  #main button{
    margin-top: 20px;
    margin-right: 20px;
    color: rgb(26, 151, 9);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 80px;
    width: 190px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
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
