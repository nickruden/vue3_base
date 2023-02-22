<script>
 export default{
  name: "App",
  data() {
    return {
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
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est perspiciatis culpa animi? Error totam laborum, doloremque maiores optio minus ipsa et laboriosam architecto assumenda nam labore ad in libero, animi cupiditate iusto veritatis. Cupiditate ipsa repellendus, earum pariatur quis nisi error voluptas aliquid, eum doloremque quas hic tempore! Nihil, et.</p>
    </div>
  </div>
  <p id="endword">by NikitaRudenko</p>
</template>

<style>
  #main{
    margin-top: 50px;
    margin-bottom: 50px;
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1100px;
    height: 500px;
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
    color: rgb(3, 114, 58);
    text-shadow: 0px 1px 10px rgb(20, 143, 81);
  }
  #main h2{
    font-size: 40px;
    margin-top: 4px;
    text-decoration: underline;
  }
  #main .p{
    font-size: 28px;
  }
  #main ul{
    margin-top: 10px;
    text-align: left;
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
  #endword{
    font-size: 30px;
    margin-top: 480px;
    margin-left: -670px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
