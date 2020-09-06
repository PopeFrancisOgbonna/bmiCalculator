<template>
  <div :class="{'hide':isActive == 0 ? false : true} ">
    <h3>Ensure You Enter Your Details Correctly.</h3>
    <form>
      <label for="name">Name:</label>
      <input type="text" v-model="userName" name="name" placeholder="Full Name" required/>
      <label for="weight">Weight (kg):</label>
      <input type="number" v-model="weight" name="weight" placeholder="Your weight in Kg" required/>
      <label for="height">Height (m):</label>
      <input type="number" v-model="height" name="height" placeholder="Your height in meters" required/>
      <p class="errMsg">{{error}}</p>
      <input id="send" type="button" v-on:click="clear" value="Calculate">
    </form>
  </div>
</template>

<script>
export default {
  name: 'Details',
  props: ['isActive'],
  data: () => {
     return {
      userName: '',
      weight: '',
      height: '',
      result: '',
      error: ''
    }
  },
  methods: {
    clear(e){
      e.preventDefault();
      if(this.userName =='' || this.weight =='' || this.height ==''){
         return this.error ="Please Fill out all Fields!";
      }else{
        this.result = this.weight * (this.height * this.height);
        const bmi = {
          'name': this.userName,
          'results': this.result
        }
        this.$emit('calculated',bmi);
        this.userName = '';
        this.weight = '';
        this.height = '';
        this.error ='';
        this.$emit('toggle');
      }
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    padding: 25px;
    margin: 5px auto;
    width: 35%;
    border: 3px solid #4e4e4e;
    border-radius: 10px;
  }
  input {
    padding: 5px;
  }
  label {
    text-align: left;
    margin-top:10px;
  }
  #send {
    background: #03aefd;
    border-style: none;
    width: 200px;
    padding: 15px;
    border-radius: 10px;
    margin: 2px auto;
    color: #fff;
    text-transform: uppercase;
    line-height: 24px;
    font-size: 1.8em;
    box-shadow: 0 0 12px #444;
  }
  #send:hover {
    cursor: pointer;
  }
  .errMsg {
    color: rgb(252, 4, 4);
  }
</style>