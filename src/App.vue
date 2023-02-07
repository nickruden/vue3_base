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
      <p>Дата {{ todaydate() }}</p>

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
  #main p,  #main h2{
    font-size: 70px;
  }
  #main h2{
    margin-top: 10px;
    text-decoration: underline;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 180px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
