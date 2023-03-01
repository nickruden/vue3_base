<script>
 export default{
  name: "Employee",
  // Ex. 2
  props: ['fname', 'lname', 'age'],

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
        <h2>Ex. 2</h2>
        <p>{{ fname }}</p>
        <p>{{ lname }}</p>
        <p>{{ age }}</p>
    </div>
</template>


<style>
    #main{
    margin-top: 50px;
    margin-bottom: 50px;
    background-color: rgb(43, 221, 117);
    color: rgb(189, 255, 177);
    width: 1100px;
    text-align: center;
    border: 10px solid rgb(43, 221, 117);
    border-radius:60px;
    text-shadow: 0px 1px 10px rgb(160, 248, 207);
  }
  #main div{
    margin-top: 10px;
    margin-bottom: 40px;
  }
  #main p{
    font-size: 24px;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  #main h2{
    font-size: 36px;
    margin-top: 4px;
    margin-bottom: 10px;
    text-decoration: underline;
  }
</style>
