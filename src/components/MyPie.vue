<template>
  <div class="float-child MyPie">
    <h1>{{ msg }}</h1>
    <canvas id="myPie" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  name: "MyPie",
  props: {
    msg: String,
  },
  mounted() {
    const ctx = document.getElementById("myPie").getContext("2d");
    const myPie = new Chart(ctx, {
      type: "pie",
      data: {
        labels: ["Red", "Blue", "Yellow"],
        datasets: [
          {
            label: "My First Dataset",
            cutout: '50%',          // 0 for pie chart
            data: [300, 50, 100],
            backgroundColor: [
              "rgb(255, 99, 132)",
              "rgb(54, 162, 235)",
              "rgb(255, 205, 86)",
            ],
            hoverOffset: 4,
          },
        ],
      },
    });
    myPie;
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.float-child {
  width: 25%;
  float: left;
  padding: 40px;
  border: 2px solid lightlightgoldenrodyellowcyan;
}
div {
  width: 400px;
  height: 400px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
