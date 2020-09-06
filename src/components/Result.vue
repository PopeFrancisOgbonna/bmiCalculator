<template>
  <div>
    <div>
      <h3>Congratulations! {{name}}</h3>
      <p>Your BMI is {{bmiValue}}</p>
      <div class="chart">
        <table>
        <tr>
          <th></th>
          <th>Underweight</th>
          <th>Normal Weight</th>
          <th>Overweight</th>
          <th>Obese</th>
          <th>Clinically Obese</th>
        </tr>
        <tr>
          <td>BMI Result</td>
          <td>15</td>
          <td>20</td>
          <td>34</td>
          <td>45</td>
          <td>Above 50</td>
        </tr>
        
      </table>
      <img id="graph" src="../assets/bmigraph.png" alt="BMI graph">
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Result',
  props:['name','bmiValue','isActive']
}
</script>

<style scoped>
  #graph {
    max-width: 85%;
  }
  td, th {
    border: 1px solid #ddd;
    text-align: left;
    padding: 8px;
  }
  tr:nth-child(even) {
    background-color: #ddd;
  }
  table {
    margin: 0 auto;
  }
</style>