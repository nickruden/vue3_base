<script>
 export default{
  name: "App",
  data() {
	return {
    //Ex. 1
		arr1: ['x', 'y', 'z'],

    //Ex. 2
    arr2: [1, 2, 3],
	  }
  }
}
</script>

<template>
    <div id="main">
      <!-- Ex. 1  -->
      <h2>Ex. 1</h2>
      <p>Первый элемент массива: {{ arr1[0] }} </p>
      <p>Второй элемент массива: {{ arr1[1] }}</p> 
      <p>Третий элемент массива: {{ arr1[2] }}</p>

      <!-- Ex. 2 -->
      <h2 id="h2">Ex. 2</h2>
      <p>Сумма элементов массива = {{ arr2[0] + arr2[1] + arr2[2] }}</p>

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
    font-size: 30px;
  }
  #main h2{
    margin-top: 10px;
    text-decoration: underline;
  }
  #h2{
    margin-top: 20px;
  }
  #main #endword{
    font-size: 30px;
    margin-top: 110px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
