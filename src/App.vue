<script>
 export default{
  name: "App",
  data() {
    // Ex. 1
    return {
      hrefs: [
			{href: '1.html', text: 'text1'},
			{href: '2.html', text: 'text2'},
			{href: '3.html', text: 'text3'},
		],

    // Ex. 2
    products: [
			{
				name: 'product1',
				price: 100,
				quantity: 5
			},
			{
				name: 'product2',
				price: 200,
				quantity: 4
			},
			{
				name: 'product3',
				price: 300,
				quantity: 3
			},
		],
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
      <div v-for="item in hrefs">
        <a href="{{ item.href }}">{{ item.text }}</a>
      </div>
    </div>

    <!-- Ex. 2 -->
    <div>
      <h2>Ex. 2</h2>
        <table> 
          <tr v-for="product in products">
		        <td>{{ product.name }}</td>
		        <td>{{ product.price }}</td>
		        <td>{{ product.quantity }}</td> 
	        </tr>
        </table>
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
    margin-top: 540px;
    margin-left: -670px;
    color: rgb(83, 100, 80);
    text-shadow: 0px 1px 10px rgb(128, 151, 141);
  }
</style>
