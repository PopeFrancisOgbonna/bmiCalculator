<template>
  <div>
    <Result :name="name" :bmiValue="bmiValue"/>
    <Recommendation @back="$emit('back')"/>
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
  props:['name','bmiValue']
}
</script>

<style>

</style>