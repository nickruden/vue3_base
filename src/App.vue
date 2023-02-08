<script>
 export default{
  name: "App",
  data() {
	return {
	  }
  },
  methods: {
    numalert: function(num) {
      alert(num ** 2);
	}
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p>Для возведения числа 12 в квадрат нажмите на кнопку</p>
      <button @click="numalert(12)">12</button>

      <p id="endword">by NikitaRudenko</p>
    </div>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1000px;
    height: 500px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:50px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  #main p{
    font-size: 40px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 10px;
    text-decoration: underline;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 150px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
  #main button{
    margin-top: 10px;
    color: rgb(26, 151, 9);
    font-size: 40px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 70px;
    width: 140px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 30px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(74, 197, 94);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
</style>
