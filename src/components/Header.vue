<template>
  <div>
     <div id="imgDiv">
       <img id="logo" src="../assets/logo.jpg" alt="BMI logo"/>
     </div>
    <h1>
       BMI Calcultor
    </h1>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
  #logo {
    width: 60px;
    height: auto;
    border-radius: 5px;
    float: left;
    padding: 5px;
  }
  h1 {
    text-transform: uppercase;
    padding: 5px;
  }
  div {
    background: #61606049;
    margin-bottom: 0;
  }
  
</style>