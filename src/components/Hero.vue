<template>
  <div class="div" :class="{'hide':isActive == null ? false : true}">
    <div class="heroContent">
      <h1>What is BMI?</h1>
      <p>
        Your BMI or Body Mass Index is a measurement of body fat based 
        on your height and weight. This health calculation applies 
        to both men and women between the ages of 18 and 65 years.
      </p>
      <p>
        BMI can be used to indicate if you are overweight, obese, 
        underweight or normal. A healthy BMI score is between 20 
        and 25. A score below 20 indicates that you may be 
        underweight; a value above 25 indicates that you may be 
        overweight.
      </p>
      <button @click="$emit('toggle')">Calculate Your BMI Now!</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: ['isActive']
}
</script>

<style scoped>
  .div {
    background: url("../assets/scale.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    height: 400px;
    text-align: center;
    margin-top: -18px;
  }
  .heroContent {
    width: 600px;
    text-align: center;
    margin: 0  auto;
  }
  h1 {
    padding-top: 10px;
  }
  button {
    padding: 15px;
    border-radius: 5px;
    color: #fff;
    background: #6bcd6b;
    border-style: none;
    font-size: 1.3em;
    margin: 15px auto;
    box-shadow: 0 0 12px #4e4e4e;
  }
  button:hover {
    cursor: pointer;
    background: lightcoral;
  }
  p {
    text-align: left;
    color: #251d1d;
    font-size: 1.3em;
  }
</style>