<script>
 export default{
  name: "App",
  data() {
	  return {
		  name: 'Nikita',
		  surn: 'Rudenko',
	}
}
 }
</script>

<template>
    <div id="main">
      <div class="div1">
      {{ name }}
      </div>
      <div class="div2">
      {{ surn }}
      </div>
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
  #main .div1, #main .div2{
    font-size: 40px;
    margin-top: 20px;
  }
  #main .div1{
    margin-top: 140px;
  }
  #main .div2{
    margin-top: -20px;
  }
</style>
