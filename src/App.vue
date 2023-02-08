<script>
 export default{
  name: "App",
  data() {

  // Ex. 1
	return {
    hidden: false,
    textbutton: 'Изменить значение свойства на true'
	  }
  },
  methods: {
    clickbutton: function(){
      this.hidden = true
    }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p v-if="!hidden">Инвертируемое условие - показано, если значение свойства hidden будет равно false</p>
      <p>Значение свойства 'hidden' равно {{ hidden }}</p>

      <button @click="clickbutton()">{{ textbutton }}</button>

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
    font-size: 35px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 8px;
    text-decoration: underline;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 80px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }

  #main button{
    margin-top: 15px;
    margin-right: 20px;
    color: rgb(26, 151, 9);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 90px;
    width: 250px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(74, 197, 94);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }

  #main a{
    font-size: 30px;
    color: rgb(57, 107, 41);
  }
  #main a:hover{
    color: rgb(233, 255, 255);
  }
</style>
