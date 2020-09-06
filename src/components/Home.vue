<template>
  <div>
  <Hero :isActive="isActive" @toggle="toggle"/>
  <Details v-on:calculated="result" :isActive="isActive" @toggle="toggle"/>
  <ResultContainer 
    :class="{'hide':isActive != 1 ? true : false}" 
    :name="name" :bmiValue="bmiValue" :isActive="isActive" 
    @back="back" @toggle="toggle"
  />
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
      isActive: null
    }
  },
  methods: {
    result(bmi){
      this.name = bmi.name;
      this.bmiValue = bmi.results
    },
    toggle(){
      this.isActive == null ? this.isActive = 0 : this.isActive == 0 ? this.isActive = 1 : this.isActive = 0;
    },
    back(){
      this.isActive = null;
    }
  }
}
</script>

<style>

</style>