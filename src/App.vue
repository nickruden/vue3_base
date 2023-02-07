<script>
 export default{
  name: "App",
 }
</script>

<template>
    <div id="main">
      <h1> Просто большие буквы </h1>
      <p> Это первое взаимодействие с блоком представления в компоненте vue</p>
      <h2> by NikitaRudenko</h2>
    </div>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(32, 80, 27);
    width: 1000px;
    height: 500px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:50px;
    text-shadow: 0px 1px 20px rgb(46, 116, 39);
  }
  #main h1, #main p{
    font-size: 40px;
  }
  #main p{
    margin-top: 90px;
  }
  #main h2{
    font-size: 30px;
    margin-top: 140px;
  }
</style>
