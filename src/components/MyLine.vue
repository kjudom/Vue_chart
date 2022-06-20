<template>
  <div class="float-child MyLine">
    <h1>{{ msg }}</h1>
    <canvas id="myLine" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from "chart.js/auto";
//import Utils from "chart.js/auto";

export default {
  name: "MyLine",
  props: {
    msg: String,
  },
  mounted() {
    const ctx = document.getElementById("myLine").getContext("2d");
    const myLine = new Chart(ctx, {
      type: "line",
      //labels: Utils.months({ count: 7 }),
      data: {
        //labels: labels,        
        labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
        datasets: [
          {
            label: "My First Dataset",
            data: [65, 59, 80, 81, 56, 55, 40],
            fill: false,
            borderColor: "rgb(75, 192, 192)",
            tension: 0.3,
          },
        ],
      },
    });

    myLine;
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
