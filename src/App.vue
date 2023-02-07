<script>
 export default{
  name: "App",
  data() {
	return {
		text: 'page',
		href: 'page.html',
	  }
  }
}
</script>

<template>
    <div id="main">
      <a :href="href">{{ text }}</a>
    </div>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(172, 255, 159);
    width: 1000px;
    height: 500px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:50px;
    text-shadow: 0px 1px 21px rgb(140, 247, 197);
  }
  #main a{
    font-size: 100px;
  }
  #main a:hover{
    color: rgb(126, 186, 255);
    text-shadow: 0px 1px 21px rgb(37, 56, 85);
  }
</style>
