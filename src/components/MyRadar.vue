<template>
  <div class="float-child MyRadar">
    <h1>{{ msg }}</h1>
    <canvas id="myRadar" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  name: "MyRadar",
  props: {
    msg: String,
  },
  mounted() {
    const ctx = document.getElementById("myRadar").getContext("2d");
    const myRadar = new Chart(ctx, {
      type: "radar",
      data: {
        labels: [
          "Eating",
          "Drinking",
          "Sleeping",
          "Designing",
          "Coding",
          "Cycling",
          "Running",
        ],
        datasets: [
          {
            label: "My First Dataset",
            data: [65, 59, 90, 81, 56, 55, 40],
            fill: true,
            backgroundColor: "rgba(255, 99, 132, 0.2)",
            borderColor: "rgb(255, 99, 132)",
            pointBackgroundColor: "rgb(255, 99, 132)",
            pointBorderColor: "#fff",
            pointHoverBackgroundColor: "#fff",
            pointHoverBorderColor: "rgb(255, 99, 132)",
          },
          {
            label: "My Second Dataset",
            data: [28, 48, 40, 19, 96, 27, 100],
            fill: true,
            backgroundColor: "rgba(54, 162, 235, 0.2)",
            borderColor: "rgb(54, 162, 235)",
            pointBackgroundColor: "rgb(54, 162, 235)",
            pointBorderColor: "#fff",
            pointHoverBackgroundColor: "#fff",
            pointHoverBorderColor: "rgb(54, 162, 235)",
          },
        ],
      },
    });
    myRadar;
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
