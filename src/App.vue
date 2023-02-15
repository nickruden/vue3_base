<script>
 export default{
  name: "App",
  data() {
  // Ex. 1
	return {
    visible1: true,
    visible2: true,
    visible3: true,
    text1: true,
    text2: true,
    text3: true
	  }
  },

  methods: {
    toggle1: function(){
      this.text1 = !this.text1,
      this.visible1 = !this.visible1
    }, 
    toggle2: function(){
      this.text2 = !this.text2,
      this.visible2 = !this.visible2
    },
    toggle3: function(){
      this.text3 = !this.text3,
      this.visible3 = !this.visible3
    }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p v-if="text1">Нажмите на кнопку 1, чтобы скрыть или показать этот абзац</p>
      <p v-if="text2">Нажмите на кнопку 2, чтобы скрыть или показать этот абзац</p>
      <p v-if="text3">Нажмите на кнопку 3, чтобы скрыть или показать этот абзац</p>
      <button @click="toggle1()">{{ visible1 ? 'Скрыть 1' : 'Показать 1'}}</button>
      <button @click="toggle2()">{{ visible2 ? 'Скрыть 2' : 'Показать 2'  }}</button>
      <button @click="toggle3()">{{ visible3 ? 'Скрыть 3' : 'Показать 3' }}</button>
    </div>
    <p id="endword">by NikitaRudenko</p>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1000px;
    height: 600px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:60px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  #main p{
    font-size: 26px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 20px;
    text-decoration: underline;
  }
  #endword{
    font-size: 30px;
    margin-top: 540px;
    margin-left: -610px;
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
    height: 60px;
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
</style>
