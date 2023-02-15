<script>
 export default{
  name: "App",
  data() {
  // Ex. 1
	return {
    hidden: false,
    text1: true,

    //Ex. 3
    text2: true,
    button1: false,
    button2: true
	  }
  },

  methods: {
    clickbutton: function(){
      this.hidden = true
    },

    // Ex. 2
    show1: function(){
      this.text1 = true
    },
    hide1: function(){
      this.text1 = false
    },

    // Ex. 3
    show2: function(){
      this.text2 = true,
      this.button1 = false,
      this.button2 = true
    },
    hide2: function(){
      this.text2 = false,
      this.button2 = false,
      this.button1 = true
    }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p v-if="hidden">Просто какой-то текст</p>
      <button @click="clickbutton()">нажми</button>

      <!-- Ex. 2  -->
      <h2>Ex. 2</h2>
      <p v-if="text1">Просто какой-то текст</p>
      <button @click="show1()">показать</button>
      <button @click="hide1()">скрыть</button>

      <!-- Ex. 3  -->
      <h2>Ex. 3</h2>
      <p v-if="text2">Просто какой-то текст</p>
      <button v-if="button1" @click="show2()">показать</button>
      <button v-if="button2" @click="hide2()">скрыть</button>

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
    font-size: 22px;
  }
  #main h2{
    font-size: 30px;
    margin-top: 8px;
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
