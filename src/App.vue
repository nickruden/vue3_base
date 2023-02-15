<script>
 export default{
  name: "App",
  data() {
    // Ex. 1, 2
    return {
      items: [1, 2, 3],
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
      <div v-for="item in items">
        <p>{{ item }}</p>
        <p class="divider"></p>
      </div>
    </div>

    <!-- Ex. 2 -->
    <div>
      <h2>Ex. 2</h2>
      <ul class="p">
        <template v-for="item in items">
          <li>{{ item }}</li>
          <li class="divider"></li>
        </template>
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
  #main div{
    margin-top: 10px;
  }
  #main p{
    font-size: 28px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  #main h2{
    font-size: 40px;
    margin-top: 20px;
    text-decoration: underline;
  }
  #main .p{
    font-size: 28px;
  }
  #main ul{
    margin-top: 10px;
    text-align: left;
  }
  #endword{
    font-size: 30px;
    margin-top: 540px;
    margin-left: -670px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
