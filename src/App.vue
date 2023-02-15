<script>
 export default{
  name: "App",
  data() {
    // Ex. 1, 2, 3, 4
    return {
      obj: {
        user1: '100$',
        user2: '200$',
        user3: '300$',
},
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
      <ul class="p" v-for="item in obj">
        <li>{{ item }} </li>
      </ul>
    </div>

    <!-- Ex. 2 -->
    <div>
    <h2>Ex. 2</h2>
      <ul class="p" v-for="(key, item) in obj">
        <li>{{ item }} - {{ key }}</li>
      </ul>
    </div>

    <!-- Ex. 3 -->
    <div>
    <h2>Ex. 3</h2>
      <ul class="p" v-for="(key, item, index) in obj">
        <li>{{ item }} - {{ key }} - {{ index }}</li>
      </ul>
    </div>

    <!-- Ex. 4 -->
    <div>
    <h2>Ex. 4</h2>
      <ul class="p" v-for="(key, item, index) in obj">
        <li>{{ item }} - {{ key }} - {{ index + 1}}</li>
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
