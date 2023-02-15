<script>
 export default{
  name: "App",
  data() {
  // Ex. 1, 2, 3
	return {
    items: [1, 2, 3, 4, 5],
    }
  },
  methods: {

  }
}
</script>

<template>
  <div id="main">
    <!-- Ex. 1 -->
    <div>
      <h2>Ex. 1</h2>
      <div class="p" v-for="item in items"> {{ item }}</div>
    </div>

    <!-- Ex. 2 -->
    <div>
      <h2>Ex. 2</h2>
      <div class="p" v-for="item in items">{{ item ** 2}}</div>
    </div>

    <!-- Ex. 3 -->
    <div>
    <h2>Ex. 3</h2>
      <ul class="p" v-for="item in items">
        <li> {{ item }} </li>
      </ul>
    </div>
  </div>
  <p id="endword">by NikitaRudenko</p>
</template>

<style>
  #main{
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1100px;
    height: 600px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:60px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
  #main p{
    font-size: 38px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 20px;
    text-decoration: underline;
  }
  #main .p{
    font-size: 24px;
  }
  #main ul{
    text-align: left;
  }
  #endword{
    font-size: 30px;
    margin-top: 540px;
    margin-left: -670px;
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
    height: 70px;
    width: 210px;
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
