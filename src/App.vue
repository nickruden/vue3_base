<script>
 export default{
  name: "App",
  data() {
  // Ex. 1
	return {
      day: new Date().getDay(),
    }
  },
  methods: {

  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p v-if = "day == 1">Сегодня понедельник</p>
      <p v-if = "day == 2">Сегодня вторник</p>
      <p v-if = "day == 3">Сегодня среда</p>
      <p v-if = "day == 4">Сегодня четверг</p>
      <p v-if = "day == 5">Сегодня пятница</p>
      <p v-if = "day == 6">Сегодня суббота</p>
      <p v-if = "day == 7">Сегодня воскресенье</p>
    </div>
    <p id="endword">by NikitaRudenko</p>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1100px;
    height: 600px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:60px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  #main p{
    font-size: 28px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 20px;
    text-decoration: underline;
  }
  #main>h2+p{
    font-size: 30px;
  }
  #endword{
    font-size: 30px;
    margin-top: 540px;
    margin-left: -670px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }

  #main button{
    margin-top: 15px;
    margin-right: 20px;
    margin-left: 30px;
    color: rgb(26, 151, 9);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 70px;
    width: 200px;
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
