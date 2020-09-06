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
  #app {
    text-align: center;
  }
  .hide {
    display: none;
  }
</style>