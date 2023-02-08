<script>
 export default{
  name: "App",
  data() {
	return {
    // Ex. 1
    cost: 10,
    amount: 140,
	  }
  },
  computed: {
    price: function(){
      return this.cost * this.amount
    }
  },

  // Ex. 2
  methods: {
    newprice: function(){
      this.cost = this.cost + 2
    }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p>Цена продукта: {{ cost }}</p>
      <p>Колличество продуктов: {{ amount }}</p>
      <p>Полная стоимость продукта: {{ price }}</p>

      <!-- Ex. 2-->
      <h2>Ex. 2</h2>
      <p>Для изменения значения цены на 2 еденицы нажмите на кнопку</p>
      <button @click="newprice">Новая цена</button>

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
    margin-top: 8px;
    text-decoration: underline;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 50px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }

  #main button{
    margin-top: 15px;
    margin-right: 20px;
    color: rgb(26, 151, 9);
    font-size: 30px;
    text-shadow: 0px 1px 10px rgb(108, 180, 84);
    background-color: rgb(66, 255, 198);
    height: 90px;
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
