<script>
 export default{
  name: "App",
  data() {
    return {
      // Ex. 1
      num1: 0,
      sqrt: 0,

      // Ex. 2
      num2: 0,
      num3: 0,
      sum: 0,

      // Ex. 3
      text1: 'Нажми на кнопку',
      text2: 'Поменяй меня',

      // Ex. 4
      fio: 'ФИО через пробел',
      fname: 'Фамилия',
      lname: 'Имя',
      sname: 'Отчество'
    }
  },
  methods: {
    // Ex. 1
    sqrtnum1: function() {
      this.sqrt = Math.sqrt(this.num1);
    },
    
    // Ex. 2
    sumnum23: function() {
      this.sum = Number(this.num2) + Number(this.num3);
    },

    // Ex. 3
    swap: function() {
      let t = this.text1
      this.text1 = this.test2;
      this.text2 = t;
    },

    // Ex. 4
    outfio: function() {
      let fios = this.fio.split(' ');
      this.fname = fios[0];
      this.lname = fios[1];
      this.sname = fios[2];
    } 
  }
}
</script>

<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1</h2>
      <p> Квадратный корень введённого числа: {{ sqrt }}</p>
      <input v-model="num1">
      <button @click="sqrtnum1">Найти корень</button>
    </div>

    <!-- Ex. 2 -->
    <div>
      <h2>Ex. 2</h2>
      <p> Сумма введённых чисел: {{ sum }}</p>
      <input v-model="num2">
      <input v-model="num3">
      <button @click="sumnum23">Найти сумму</button>
    </div>

   <!-- Ex. 3 -->
   <div>
    <h2>Ex. 3</h2>
    <input class="inptext" v-model="text1"> <br>
    <input class="inptext" v-model="text2"> <br>
    <button @click="swap">Поменять</button>
   </div>

   <!-- Ex. 4 -->
   <div>
    <h2>Ex. 4</h2>
    <p>Фамилия: {{ fname }}</p>
    <p>Имя: {{ lname }}</p>
    <p>Отчество: {{ sname }}</p>
    <input class="inpfio" v-model="fio"> <br>
    <button @click="outfio">Вывести</button>
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
    margin-top: 20px;
    margin-bottom: 10px;
  }
  #main h2{
    font-size: 36px;
    margin-top: 4px;
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
    height: 50px;
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
    width: 100px;
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

  #endword{
    font-size: 30px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
