<template>
  <div>
  <Hero :showHero="showHero"/>
  <Details v-on:calculated="result" :showDetails="showDetails"/>
  <ResultContainer @back="back" :name="name" :bmiValue="bmiValue" :showResult="showResult"/>
  <Footer/>
  </div>
</template>

<script>
import Hero from './Hero';
import Details from './Details';
import Footer from './Footer';
import ResultContainer from './ResultContainer';
export default {
  name: 'Home',
  components: {
    Hero,
    Details,
    Footer,
    ResultContainer
  },
  data:() =>{
    return {
      name: '',
      bmiValue: '',
      showHero: false,
      showDetails: true,
      showResult: true
    }
  },
  methods: {
    result(bmi){
      this.name = bmi.name;
      this.bmiValue = bmi.results
    },
    back(e){
      e.preventDefault();
      this.showHero = false;
    }
  }
}
</script>

<style>

</style>