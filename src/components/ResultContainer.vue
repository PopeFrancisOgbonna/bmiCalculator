<template>
  <div>
    <Result :name="name" :bmiValue="bmiValue" />
    <Recommendation :isAtive="isActive"
      @back="$emit('back')" @toggle="$emit('toggle')"
    />
  </div>
</template>

<script>
import Result from './Result';
import Recommendation from './Recommendation';
export default {
  name: 'ResultContainer',
  components: {
    Result,
    Recommendation
  },
  props:['name','bmiValue','isActive'],
  data(){
    return{

    }
  },
  methods: {
    
  }
}
</script>

<style>

</style>