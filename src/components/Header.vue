<template>
  <div>
    <span>
      <img id="logo" src="../assets/logo.jpg" alt="BMI logo"/>
      <h1>BMI Calcultor</h1>
    </span>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
  #logo {
    height: 60px;
    width: 60px;
    border-radius: 25%;
    margin-bottom: 0;
    margin-top: 5px;
  }
  h1 {
    margin-top: auto 5px;
    text-transform: uppercase;
    padding: 5px;
  }
  div {
    background: #61606049;
    margin-bottom: 0;
    width: 100%;
    color: #fff;
  }
  span {
    display: flex;
    justify-content: center;
  }
</style>