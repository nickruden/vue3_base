<script>
 export default{
  name: "App",
  data() {
	return {
    //Ex. 1
		num: 5,

    //Ex. 2
    num1: 1,
		num2: 2,
		num3: 3,
	  }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>1) Квадрат из числа 5 = {{ num ** 2 }}</h2>

      <!-- Ex. 2 -->
      <h2>2) Сумма чисел {{ num1}}, {{num2 }}, {{ num3 }} равна {{ num1 + num2 + num3 }}</h2>

      <p>by NikitaRudenko</p>
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
  #main h2{
    font-size: 40px;
    margin-top: 20px;
  }
  #main p{
    font-size: 30px;
    margin-top: 240px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
