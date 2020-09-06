<template>
  <div id="recDiv">
    <h3>Recommendations</h3>
    <div class="container">
      <div class="suggestion">
        <h4>How to Improve your BMI Results </h4>
        <p>
          Meal plans and healthy food delivery adapted to your nutrition 
          needs is a great place to start! 
          Good dietry plan can help you improve your Body Mass Index within a short time 
          Interval and help you reduce the risk of illness.
        </p>
        <div class="inner-wrap">
          <div>
            <h5>Eat Fitness Foods</h5>
            <p>Fitness meal plans with ingredients 
              as close to natural as possible can 
              help your BMI score.
            </p>
          </div>
          <div>
            <h5>Nutritionist Crafted Meals</h5>
            <p>
              Get targeted meals that are focused 
              towards improving your bmi score and 
              that are delicious. Check them out here.
            </p>
          </div>
          <div>
            <h5>Drink lots of Water</h5>
            <p>
              Replaced the sugared drinks with still or sparkling water, 
              removing excess calories will help your BMI.
            </p>
          </div>
          <div>
            <h5>Regular Exercise</h5>
            <p>
              Getting regular exercie 2-3 days per week is 
              recommended to achieve a healthy lifestyle.
            </p>
          </div>
        </div>
      </div>
      <div class="img">
        <img id="meal" src="../assets/meal.jpg" alt="Meal">
      </div>
    </div>
    <div>
      <button @click="$emit('back')">Back</button>
      <button>Perform another Calculation</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Recommendation'
}
</script>

<style scoped>
  #recDiv {
    margin-left: 4%;
  }
  .container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin:2% 3%;
  }
  .suggestion {
    width: 46%;
    text-align: justify;
  }
  .img {
    width: 5%;
    margin:0 0 0 6%;
    height: 450px;
  }
  #meal {
    max-height: 100%;
    width: auto;
    margin: 10px;
  }
  .inner-wrap {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
  }
  .inner-wrap  div {
    width: 200px;
    text-align: center;
  }
  button {
    padding: 5px;
    margin: 5px 20px;
  }
  button:hover {
    cursor: pointer;
  }
</style>