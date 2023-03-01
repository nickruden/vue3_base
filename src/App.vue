<script>
 export default{
  name: "App",
  data() {
    return {
      // Ex. 1
      text1: ' ',

      // Ex. 2
      text2: 'Просто какой-то текст',

      // Ex. 3
      pushed: false,
      text3: ' ',
    }
  },

  methods: {
    // Ex. 1
    submit: function () {
      this.text1 = this.$refs.text1.value;
    }, 

    // Ex. 2
    ctrl: function (event) {
      if (event.ctrlKey) {
        this.pushed = true;
      }
    },

    // Ex. 3
    right: function (event) {
      if (!event.ctrlKey) {
        this.text3 = 'Правая кнопка мыши';
      }
    },
    left: function (event) {
      if (!event.ctrlKey) {
        this.text3 = 'Левая кнопка мыши';
      }
    },
    middle: function (event) {
      if (!event.ctrlKey) {
        this.text3 = 'Средняя кнопка мыши';
      }
    }
  }
}
</script>

<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1</h2>
      <input type="text" @keyup.enter="submit" ref="text1">
      <p>{{ text1 }}</p>
    </div>

    <!-- Ex. 2 -->
    <div>
      <h2>Ex. 2</h2>
      <a href="#" @click="ctrl"> Ссылка </a>
      <p v-if="pushed">{{ text2 }}</p>
    </div>

    <!-- Ex. 3 -->
    <div>
      <h2>Ex. 3</h2>
      <a href="#" @click.right="right" @click.left="left" @click.middle="middle"> Ссылка </a>
      <p>{{ text3 }}</p>
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
  #main .p{
    font-size: 28px;
  }
  #main .pinput{
    text-transform: uppercase;
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
    height: 55px;
    width: 150px;
    border: 4px solid rgb(74, 197, 94);
    border-radius: 40px;
  }
  #main button:hover{
    color: rgb(57, 107, 41);
    background-color: rgb(20, 167, 45);
    border: 4px solid rgb(66, 255, 198);
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  
  #main input{
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
  #main .inptext{
    margin-top: 10px;
    font-size: 20px;
    width: 400px;
    height: 40px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    text-align: center;
    margin-right: 10px;
  }
  #main .inpfio{
    margin-top: 10px;
    font-size: 20px;
    width: 400px;
    height: 40px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    text-align: center;
    margin-right: 10px;
  }

  #main textarea{
    margin-bottom: -10px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    padding: 10px;
    margin-right: 10px;
  }

  #main .checkboxs{
    font-size: 20px;
  }

  #main select{
    margin-top: 10px;
    margin-bottom: 5px;
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(19, 151, 61, 0.616);
    color: rgb(131, 255, 214);
    font-size: 20px;
    text-shadow: 0px 1px 10px rgb(0, 255, 136);
    padding: 10px;
    margin-right: 10px;
  }
  #main select:hover{
    border-radius: 20px;
    border: 4px solid rgb(238, 255, 250);
    background-color: rgba(38, 116, 64, 0.616);
    color: rgb(131, 255, 214);
  }

  #endword{
    font-size: 30px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
