<template>
  <div id="app">
    <Header/>
    <Home />
  </div>
</template>

<script>
import Header from './components/Header';
import Home from './components/Home'
export default {
  name: 'App',
  components: {
    Header,
    Home
  }
}
</script>

<style>
body{
  margin: 0 5px;
  padding: 0;
}
  #app {
    text-align: center;
  }
  .hide {
    display: none;
  }
</style>