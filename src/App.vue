<script>
 export default{
  name: "App",
  data() {
	return {
	  }
  },
  methods: {
    todaydate: function() {
      var d = new Date();
      alert("Today: " + d.toDateString());
	}
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p>Нажми</p>
      <button @click="todaydate">Date</button>

      <!-- Ex. 2  -->
      <h2>Ex. 2</h2>
      <p>Наведи</p>
      <button @mouseenter="todaydate">Date</button>
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
    font-size: 25px;
  }
  #main h2{
    font-size: 30px;
    margin-top: 5px;
    text-decoration: underline;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 90px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }

  #main button{
    font-size: 40px;
    color: rgb(26, 151, 9);
    text-shadow: 0px 1px 10px rgb(90, 223, 112);
    background-color: rgb(66, 255, 198);
    height: 80px;
    width: 160px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(74, 197, 94);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
</style>
